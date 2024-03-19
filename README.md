
## Demos Of Audio Tools/Components

As my new portfolio website is still in progress, here I list part of my development tools in demo version. More tools' demos will be released in future updates.

### Wwise Auto Switch Assignment Plugin
<https://youtu.be/mUuQFkw_r5c>

This tool is developed to allow audio designers to quickly assign switch units to their parent switch containers according to a defined rule. The plugin is developed with the JUCE framework and WAAPI, and users can install it directly into the Wwise editor.

Usually in Wwise, a designer has to drag the switch units to the switches one by one, which is time-consuming when a large number of switches need to be integrated. With the plugin, users can select multiple switch containers at the same time, assign them to a switch/state group (the plugin will automatically collect all the switch/state groups in the project), and automatically assign their child containers to each switch based on a specific rule. In this demo video, the matching rule is to let the middle word or suffix of the child switch container match the switch name. Other matching rules are still welcome to be applied to the plugin.

The plugin holds the design idea of "partial automation", providing flexibility to the integrators and allowing them to customize the operating unit. It simplifies the integration process with just a few clicks on the designed UI and adapts to common situations when users need to make switch assignments. No matter how many switch containers with different types of switches need to be handled, or even if there are nested switch structures to deal with, the plugin makes the integration process much easier.

### Dynamic Spacial Audio Component Demo
<https://youtu.be/UcmTNhhbLqU>

This component is a new solution to implement the spatial audio effect in a dynamic space. It is developed as an actor component in the Unreal engine, with the API of the Wwise Unreal integration.

The main idea of this component is to assume that the room around the character is dynamically changing in volume and shape as the character keeps moving in the world. Thus, a fixed aux channel set in a room is not suitable for this situation. Instead, the model splits the space around the character into planes. It calculates the relative distance of each plane to generate a plane pattern. Based on the shape of the plane pattern and the approximated volume, the component will send the spatial data as RTPCs to the Wwise audio engine, triggering the corresponding audio parameters set by the designer.

With the designed plane pattern, the relative position of the character in the current space can be located. We can now know if the character is in the corner of the room or in the middle of the room. This information can help shape the details of the spatial rooms. Among the current solutions, it is usually assumed that all acoustic features are uniform in one fixed room. Usually, only one set of effects (reverb, delay, etc.) is applied to a space. Using this model, the designer can specify the acoustic features in different parts of the room. The additional parameters provided by the component can control the diffraction rate within the reverb effect, the delay panning direction if the character is in the corner of a large space, or the volume ratio of the aux channels.

The demo video shows an example of a dynamic spatial effect made by this solution. The voices of the character are sampled from the marine unit in Starcraft2. The component in the game detects the relative position of the main character. If the character moves close to the corner, the component will send parameters to the Wwise audio engine and adjust the reverb panning of the current space, making the corner direction less reverberant and the open direction more reflective. More detailed acoustic settings are still applicable to the scene.