
## Demos Of Audio Tools/Components

As my new portforlio website is still in progress, here I list part of my development tools in demo version. More tools' demos will be released in the future update.

### Wwise Auto Switch Assignment Plugin
<https://youtu.be/mUuQFkw_r5c>

The tool is developed to let the audio designers quickly assign switch units to their parent switch container according to a defined rule. The plugin is developed with JUCE framework and WAAPI, the user can install it directly in the Wwise editor.

Usually in Wwise, a designer has to drag the swith units to the switches one by one, which is time comsuming when there are a large amount of switches needed to integrate. Using the plugin, the user is able to select multiple switch containers at the same time, and assign them to a switch/state group (the plugin will self collect all the switch/state groups in the project), and automatically assign their children container to each switch based on a specific rule. In this demo video, the matching rule is to let the middle word or suffix of the children switch container match the switch name. Other match rules are still welcomed to applied to the plugin.  

The plugin holds the design idea of "partial automation", providing flexibility to the integrators and let them costomize the operation unit. It simplified the integration step by just several clicks on the designed UI and adapt to the common situation when the user needs to make switch assignments. No matter how many switch containers with different types of switches needs to be done, or even there exist nested switches structures to deal with, the plugin will make the integration process much easier.

### Dynamic Spacial Audio Component Demo
<https://youtu.be/UcmTNhhbLqU>

This component is a new solution to implement the spacial audio effect in a dynamic space. it is developed as an actor component in Unreal engine, with the API of Wwise Unreal integration.

The main idea of this component is to suppose the room around the character is dynamically changing in volume and shape. Thus the 