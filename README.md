
The human visual system is not a passive recorder of the world but an active interpreter of sensory input. Our perception is shaped by the way neurons in the eye and brain process information, rather than by the raw physical properties of light. As a result, certain optical illusions emerge because of how our neural circuits enhance, suppress, or modify visual data. In this project, MATLAB-based computational models are used to simulate neural responses to visual stimuli, focusing on two well-known illusions: the Mach Band Illusion and the Hermann Grid Illusion.

Through image processing techniques that mimic the functions of the retina and the primary visual cortex (V1), we gain insight into how the brain detects edges, patterns, and contrasts. This essay explores how these illusions arise, why they matter in neuroscience, and how they are modeled computationally.

The Mach Band Illusion: The Retina’s Role in Edge Detection
One of the most fundamental functions of the visual system is edge detection, which helps the brain distinguish objects from their surroundings. The Mach Band Illusion is a striking example of how our retina enhances contrast at edges, making bright areas seem brighter and dark areas seem darker than they really are. This illusion is a direct result of lateral inhibition, a process by which retinal ganglion cells suppress their neighbors to improve contrast sensitivity.

Generating the Mach Band Illusion
In MATLAB, the Mach Band Illusion was recreated by generating an image with a smooth gradient. Instead of perceiving a seamless transition, the human visual system exaggerates the contrast at boundaries between light and dark areas, leading to the illusion. This effect was measured by extracting a horizontal slice of brightness values, revealing a clear contrast enhancement where none physically exists in the raw image data.

Retinal Ganglion Cells and Lateral Inhibition
The illusion was further explored by simulating the behavior of retinal ganglion cells, the neurons responsible for early visual processing. These cells have a center-surround receptive field structure, meaning that they do not simply register light intensity but instead detect changes in brightness.

Each ganglion cell is sensitive to a small portion of the visual field and processes stimuli through:

An excitatory center that responds to light.
An inhibitory surround that suppresses signals from neighboring regions.
This configuration is crucial for enhancing edges and detecting contrast, enabling the brain to identify object boundaries more effectively. To model this behavior, a Difference of Gaussians (DoG) function was implemented, simulating how the receptive field of a retinal ganglion cell responds to an image.

Convolution and Neural Processing of Visual Information
To confirm that neuronal processing is responsible for the illusion, a mathematical operation known as convolution was applied to the gradient image using the receptive field model. The result showed that contrast enhancement occurred precisely at the edges, validating the role of lateral inhibition in early vision. This process, which happens in the retina before information reaches the brain, is essential for detecting important visual features such as shadows, object edges, and depth cues.

By applying computational models, this project demonstrates that our perception of reality is not an exact reflection of light patterns but is actively constructed by neural mechanisms designed to optimize our ability to detect meaningful stimuli.

The Role of the Primary Visual Cortex (V1) in Pattern Recognition
Once the retina processes visual information, it sends signals to the primary visual cortex (V1), located in the occipital lobe. This brain region is responsible for detecting edges, orientations, and textures, which allow us to recognize objects, movement, and spatial relationships.

Gabor Filters: Simulating V1 Neurons in MATLAB
Neuroscientific research has shown that V1 neurons are selectively tuned to specific orientations and spatial frequencies. These neurons function like biological filters, responding more strongly to particular patterns, such as vertical, horizontal, or diagonal edges. This property can be computationally modeled using Gabor filters, which mimic the response patterns of V1 neurons.

In MATLAB, a Gabor function was applied to an image of a rose, revealing how different settings influenced edge detection:

When the orientation (OR) was set to π/2, the filter enhanced horizontal edges.
When OR was set to π/4, diagonal patterns became prominent.
Spatial frequency (SF) changes affected the sharpness of detected edges, with lower SF emphasizing finer details and higher SF capturing broader contrast differences.
This experiment confirmed that the brain selectively processes visual information to highlight meaningful features, rather than transmitting raw visual input. This selectivity is crucial for depth perception, motion detection, and facial recognition.

The Hermann Grid Illusion: Understanding Lateral Inhibition in Perception
Another important aspect of vision is contrast perception, which is responsible for the Hermann Grid Illusion. This illusion consists of a grid of black squares separated by white lines, where illusory gray dots appear at the intersections but disappear when directly fixated upon.

Why Does This Illusion Occur?
Like the Mach Band Illusion, the Hermann Grid Illusion arises due to lateral inhibition in retinal ganglion cells. At the intersections of the white lines, each cell receives inhibition from multiple neighboring regions, reducing perceived brightness and causing the illusory gray dots. However, when looking directly at an intersection, receptive fields become smaller, reducing the effect.

Simulating the Hermann Grid Illusion in MATLAB
To explore this phenomenon computationally, a retina function was created in MATLAB, modifying parameters such as receptive field size and inhibition strength. The illusion disappeared when lateral inhibition was reduced, confirming that it is a product of neuronal processing, not an actual feature of the image.

Significance of Lateral Inhibition in Vision
Lateral inhibition is not an error in perception—it serves a vital purpose in edge enhancement and contrast detection. This mechanism allows humans to:

See objects clearly even in low-contrast environments.
Identify fine details in complex scenes.
Quickly detect movement and changes in light intensity.
By understanding illusions like the Hermann Grid, researchers gain insight into how visual processing optimizes our perception of the world while occasionally producing artifacts that do not correspond to reality.

Conclusion: How Computational Models Reveal the Mechanisms of Vision
This project demonstrates that visual perception is an active process shaped by neural computations rather than passive light detection. By simulating the Mach Band Illusion, Gabor filtering in V1, and the Hermann Grid Illusion, this study highlights:

The Role of the Retina – The Mach Band Illusion shows how retinal ganglion cells enhance contrast at edges.
The Function of V1 Neurons – Gabor filters reveal how V1 neurons selectively process orientations and spatial frequencies.
Lateral Inhibition in Perception – The Hermann Grid Illusion illustrates how neuronal suppression shapes what we see.
These findings not only enhance our understanding of biological vision but also have applications in computer vision, artificial intelligence, and medical imaging. Many image processing algorithms are inspired by these biological mechanisms, demonstrating the power of neuroscience in shaping modern technology.

By exploring these illusions computationally, we gain deeper insight into how our brains construct the reality we perceive, proving that what we see is not always what exists—but what our neurons interpret for us.





