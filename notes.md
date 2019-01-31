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

Currently, functions in WebAssembly can only use numbers (integers or floating point numbers) as parameters or return values.
For any data types that are more complex, like strings, you have to use the WebAssembly module’s memory.
(Things start getting trickier for those unfamiliar with memory management). 
This process is similar to memory management in languages like C, C++.

WebAssembly is faster than JavaScript in many cases because:

fetching WebAssembly takes less time because it is more compact than JavaScript, even when compressed.
decoding WebAssembly takes less time than parsing JavaScript.
compiling and optimizing takes less time because WebAssembly is closer to machine code than JavaScript and already has gone through optimization on the server side.
reoptimizing doesn’t need to happen because WebAssembly has types and other information built in, so the JS engine doesn’t need to speculate when it optimizes the way it does with JavaScript.
executing often takes less time because there are fewer compiler tricks and gotchas that the developer needs to know to write consistently performant code, plus WebAssembly’s set of instructions are more ideal for machines.
garbage collection is not required since the memory is managed manually.

Article links
https://medium.com/beginners-guide-to-mobile-web-development/introduction-to-web-assembly-6cb6466a3478
https://hacks.mozilla.org/2017/02/creating-and-working-with-webassembly-modules/
https://medium.freecodecamp.org/get-started-with-webassembly-using-only-14-lines-of-javascript-b37b6aaca1e4

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
