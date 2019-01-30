_How does Web Assembly fit into the web platform_ 

"The web platform can be thought of as having two parts:

 A virtual machine (VM) that runs the Web app’s code, e.g. the JavaScript code that powers your apps.
 A set of Web APIs that the Web app can call to control web browser/device functionality and make things happen
  (DOM, CSSOM, WebGL, IndexedDB, Web Audio API, etc.).
 Historically, the VM has been able to load only JavaScript.
 This has worked well for us as JavaScript is powerful enough to solve most problems people have on the Web today.
 We have run into performance problems, however, when trying to use JavaScript for more intensive use cases like 3D games,
 Virtual and Augmented Reality, computer vision, image/video editing, and a number of other domains that demand native performance."

"Since JavaScript has complete control over how WebAssembly code is downloaded, compiled and run, JavaScript developers
could even think of WebAssembly as just a JavaScript feature for efficiently generating high-performance functions."

(MDN)

!Note: Most WebAssembly module developers will code in languages like C and Rust and then compile to WebAssembly, 
but there are other ways to create a WebAssembly module. For example, there is an experimental (early-stage) tool that helps you 
build a WebAssembly module using TypeScript, or you can code in the text representation of WebAssembly directly.

LLVM - The compiler tool chain that currently has the most support for WebAssembly.
Can be a bit challenging to use directly

Emscripten - easier tool, uses LLVM under the hood

Article links
https://medium.com/beginners-guide-to-mobile-web-development/introduction-to-web-assembly-6cb6466a3478
https://hacks.mozilla.org/2017/02/creating-and-working-with-webassembly-modules/

Video
https://www.youtube.com/watch?v=6v4E6oksar0&feature=youtu.be&t=31m55s

Awesome compare between speed of JS / WASM / ASM(?)
https://github.com/Web-Sight/WebSight/tree/v1.0/src

WASM explorer
http://mbebenita.github.io/WasmExplorer/

Official demo (game by Unity using WebAssembly)
https://webassembly.org/demo/Tanks/

WebAssembly modules using TS
https://github.com/rsms/wasm-util
