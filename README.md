# Particle Simulation

This code implements a simple particle simulation in Rust using the `piston_window` and `rand` libraries. The simulation creates a 2D world with particles that move, update, and are rendered on the screen.

## Prerequisites

Make sure you have Rust and Cargo installed on your system.

## Running the Code

1. Clone the repository:

   ```bash
   git clone https://github.com/alihan-tadal/rust-particles.git
   ```

2. Navigate to the `rust-particles` directory:

   ```bash
   cd rust-particles
   ```

3. Build and run the code:

   ```bash
   cargo run
   ```

   This will compile and execute the code, opening a window to display the particle simulation.

## Description

The code is divided into several parts:

- The `World` struct represents the simulation world and contains information such as the current turn, the list of particles, and the width and height of the world.

- The `Particle` struct represents an individual particle and contains properties such as position, velocity, acceleration, size, and color.

- The `World` struct has methods to add and remove particles, update the simulation state, and draw the particles on the screen.

- The `run_guarded` function provides a thread-safe mechanism to execute a closure while guarding against simultaneous execution from multiple threads.

- The `ReportingAllocator` struct and its implementation define a custom global allocator that reports the time taken for memory allocations.

- The `main` function initializes the world, creates a window using the `piston_window` library, and runs the simulation loop. In each iteration of the loop, the world is updated and the particles are drawn on the screen.

## Dependencies

The code uses the following external dependencies:

- `graphics`: Provides basic 2D graphics primitives and transformations.
- `piston_window`: Provides a simple windowing and event handling abstraction.
- `rand`: Provides utilities for generating random numbers.
- `std`: Standard library modules such as `alloc`, `time`, and `cell`.

Please ensure that you have these dependencies installed before running the code.
