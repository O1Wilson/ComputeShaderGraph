# Complex Unity GPU Visualizations

This repository showcases my Unity development skills through two cutting-edge systems that utilize both GPU and CPU optimizations:

1. **Compute Shader 3D Graph Visualizer**  
2. **Fractal Generation System using Burst and Jobs**

---

## Overview

### Compute Shader 3D Graph Visualizer
- **What It Does:**  
  Dynamically renders an animated 3D graph/shape by calculating a grid of cube positions on the GPU. The graph is defined by various mathematical functions (e.g., Wave, MultiWave, Ripple, Sphere, Torus) that can transition smoothly between each other.
  
- **Key Features:**
  - **Dynamic Function Transitions:** Seamlessly morphs between multiple mathematical functions.
  - **Position-Based Coloring:** Alters each cube’s color based on its world position.
  - **GPU Compute Shaders:** Offloads heavy position calculations to the GPU for real-time performance.
  - **Procedural Instancing:** Uses `Graphics.DrawMeshInstancedProcedural` to efficiently render thousands of instances.

### Fractal Generation System
- **What It Does:**  
  Generates intricate, recursive fractal structures with dynamic rotations and positions, showcasing a complex hierarchy of fractal parts.
  
- **Key Features:**
  - **High-Performance Computations:** Leverages the Burst Compiler and Job System for parallel fractal updates.
  - **Recursive Data Structure:** Uses NativeArrays to manage a hierarchy of fractal parts.
  - **Dynamic Transformations:** Each fractal part is updated with rotation, sag, and spin effects to create a vivid animated structure.
  - **Procedural Instancing & Compute Buffers:** Efficiently renders fractal components with dynamic color blending based on level-specific gradients.

---

## Project Structure

- **GPUGraph.cs & Associated Compute Shaders:**  
  Handles the computation of positions for the 3D graph, dispatching compute shader kernels, and managing smooth transitions between various mathematical functions.

- **Fractal.cs & Fractal Shader Files:**  
  Implements fractal generation using Unity’s Burst and Job System. It calculates fractal part transformations in parallel and uses procedural instancing for rendering, with dynamic color interpolation across fractal levels.

- **Shaders:**  
  Custom shaders for both systems handle dynamic coloring and material properties based on the computed data.

---

## How to Run

1. **Setup the Scene:**
   - Open the project in Unity (ensure you are using a version that supports compute shaders, Burst, and the Job System).
   - For the **Graph Visualizer**:
     - Create an empty GameObject and attach the `GPUGraph` script.
     - Assign the compute shader, material (using the custom graph shader), and mesh via the Inspector.
   - For the **Fractal System**:
     - Create another GameObject and attach the `Fractal` script.
     - Configure the fractal depth, meshes, materials, color gradients, and other parameters through the Inspector.

2. **Configuration:**
   - Adjust parameters like grid resolution, function and transition durations for the graph.
   - Tweak fractal depth, spin speeds, and color gradients for the fractal system to explore various visual effects.

3. **Play the Scene:**
   - Run the scene in the Unity Editor to see both the animated 3D graph and the fractal visualization in action.
   - Experiment with parameters at runtime to fully explore the capabilities of both systems.

---

## Skills Demonstrated

- **GPU Compute Shaders:**  
  Offload complex position calculations to the GPU for real-time rendering of thousands of instances.

- **Burst Compiler & Job System:**  
  Use parallel processing to efficiently update a recursive fractal structure with high performance.

- **Procedural Instancing:**  
  Render massive amounts of geometry with minimal performance overhead using GPU instancing techniques.

- **Advanced Shader Programming:**  
  Create custom shaders that dynamically adjust colors and material properties based on position and fractal data.

- **Mathematical & Algorithmic Expertise:**  
  Implement a variety of mathematical functions for both graph visualizations and fractal generation, demonstrating a deep understanding of real-time procedural animation techniques.

---

## Conclusion

This repository is a showcase of Unity techniques for real-time visualizations. By combining compute shaders, Burst-compiled jobs, and procedural instancing, it demonstrates a robust and high-performance approach to both animated graph rendering and fractal generation. This project not only highlights my technical abilities in Unity but also my commitment to optimizing performance and creating visually compelling interactive experiences.

This project represents the culmination of my past two months of learning, applying everything from GPU programming to multithreading techniques in Unity to create high-performance visualizations.
