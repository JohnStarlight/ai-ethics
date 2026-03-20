# AI as Learning Amplifier
## Phase 1
If we're talking about 10 devices, I'd prefer the RPL routing protocol. This is extremely useful in such a scenario where battery life may or may not be an issue. I don't really know what I'm asked to design so I'm going for what makes the most sense for the most cases. 

A proactive routing protocol is great when there is stable power. Speedier and always on. 
A reactive routing protocol is the best when needed in long intervals. Saves energy. A bit slow to communicate at first in order to establish the connection.
An RPL protocol is the sweet spot between the two so we get both performance and energy saving. It builds a tree (DODAG).

## Phase 2
Having discussed this with an LLM (see notes), I have come to several conclusions and breakthroughs. 

## Phase 3
If I were to design what this exercise is asking for, I would do the following: 
For a 1000 IoT sensors I would choose RPL because of the energy efficiency. I could choose reactive as well but since I don't have the nature of the sensors, RPL is the safest choice. Probably within a mesh topology in order to ensure that even if one node fails, the rest will provide sufficient routes to continue the communication. 
For 50 traffic lights, proactive protocol within a mesh topology. Proactive because it is always on and connected and mesh to avoid a node failure. Considering the nature of the traffic lights, exposed to the elements and to possible acciddents, this is the safest choice.
For 10 emergency vehicles I would choose proactive protocol again because of the urgent nature of the service these vehicles provide. Always on with a mesh topology to stay connected. 
Considering the failure point, what I didn't consider and the LLM helped me to was that a single gateway is a single point of failure. That means that if it crashes, the network is down. To address this, introducing more gateways in standby is the best practice.

## Reflection 
My % of thought vs the LLMs is about 60-40. I chose the topology and the protocols which were given to me by the LLM. I didn't know of them before that but after reading about them, I was able to make informed choices. 
Having made these informed choices means I do understand the logic behind each protocol I listed and used and can indeed defend my choices against other options available. 
In 6 months I will remember the different types of protocols and their advantages and disadvantages. Also, the mesh topology. Perhaps I might not remember acronyms but the core knowledge of the concepts will be there.
It deffinitely made me sharper. I used the LLM to gather information and get advice in order to make the choices I made with confidence, having considered the options available, the good and the bad.