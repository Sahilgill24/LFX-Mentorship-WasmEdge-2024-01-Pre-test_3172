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
now adding burn as a dependancy and choosing ```wgpu``` as our backend framework 

```
cargo add burn --features wgpu 
cargo build 

```

now add the code snippet from Burn book https://burn.dev/book/getting-started.html

![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%207.16.56%20PM.png)



now for running the app use 

``` 
cargo run 
```


![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%207.18.08%20PM.png)

#### Now trying the text classification example of burn  again using ```wgpu```backend  

```
git clone https://github.com/tracel-ai/burn.git
cd burn
```

![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%207.22.35%20PM.png)
```
cargo run --example ag-news-train --release --features wgpu   # Train on the ag news dataset
cargo run --example ag-news-infer --release --features wgpu   # Run inference on the ag news dataset
```

![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%209.23.28%20PM.png)









### 2. ```Rustls``` building and testing 

Install WasmEdge and Cmake 

```
# install WasmEdge
curl -sSf https://raw.githubusercontent.com/WasmEdge/WasmEdge/master/utils/install.sh | bash

#set up rust compiler's target
rustup target add wasm32-wasi

# install cmake
brew install cmake

```






![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%209.56.39%20PM.png)

```
git clone https://github.com/WasmEdge/WasmEdge.git
cd WasmEdge/plugins/wasmedge_rustls
cargo build --release
```

copy target to plugin path
```
cp libwasmedge_rustls.so  ~/.wasmedge/plugin/
```



Run and test demo with pluggin 


```
# clone demo and build
git clone https://github.com/WasmEdge/wasmedge_hyper_demo
cd wasmedge_hyper_demo/client
rustup target add wasm32-wasi
cargo build --target wasm32-wasi --release

# run target with wasmedge
wasmedge run ./target/wasm32-wasi/release/wasmedge_hyper_client.wasm

```

![App Screenshot](https://github.com/Sahilgill24/LFX-Mentorship-WasmEdge-2024-01-Pre-test_3172/blob/main/images/Screenshot%202024-02-12%20at%2010.10.51%20PM.png)




heellooo jjiii 
these cahnges are done bu me i remember git































