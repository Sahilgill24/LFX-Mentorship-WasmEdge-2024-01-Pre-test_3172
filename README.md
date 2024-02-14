## LFX-Mentorship 2024-01 Pre-test

This is the pretest for WasmEdge LFX Mentorship .


### 1. Burn pretest

Install rust on your device

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```

Initializing the burn app 

```
cargo new burnapp
cd burnapp 

```
now adding burn as a dependancy and choosing wgpu as our backend framework 

```
cargo add burn --features wgpu 
cargo build 

```

now add the code snippet from Burn book 

![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%207.16.56%20PM.png)

