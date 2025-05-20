This project uses a compute shader in Unity to render a 3D graph made up of geometric shapes. Each cube in the graph is positioned on the GPU based on mathematical functions like waves, ripples, and spheres. I wrote an HLSL shader to color the cubes based on their position, which adds depth and variation across the surface.

For the fractal system, I used Unity’s Job System to handle updates across a large recursive structure. This let me animate complex transformations like rotation and sway without tanking performance. I also added color variation using another HLSL shader, so the fractal would look more organic and less uniform.

---

## Project Pictures

![detailed-sphere](https://github.com/user-attachments/assets/9119987e-9c0c-48a0-862c-9a5ab788385a)

![detailed-torus](https://github.com/user-attachments/assets/f49ddcb5-34ea-448a-bda9-94a1dc450e78)

https://github.com/user-attachments/assets/15d2ba39-8afe-4f68-8cf0-d0b0e703ac62

![variable-max-sage-angle](https://github.com/user-attachments/assets/742827cc-e65a-4eb7-9a5a-2033b49f074a)

https://github.com/user-attachments/assets/76f683bb-1d17-4598-944f-39300bbf7b1d

---

## Acknowledgements

This project was created with the help of tutorials from [CatLikeCoding](https://catlikecoding.com/) by Jasper Flick. Their in-depth explanations and guidance were invaluable in understanding procedural generation, Unity's Burst compiler, and GPU instancing.
