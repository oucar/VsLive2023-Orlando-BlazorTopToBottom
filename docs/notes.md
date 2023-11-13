### VSM01 - Workshop: Blazor Top to Bottom
- JavaScript was the only language that could run on the web some while ago, but now it's possible with C#, or more specifically Blazor.
- **Polyglot Programming**: Polyglot programming is the practice of writing code in multiple languages to capture additional functionality and efficiency not available in a single language. 
---
- **Web Assembly**: WebAssembly is a type of code that can be run in modern web browsers — it is a low-level assembly-like language with a compact binary format that runs with near-native performance and provides languages such as C/C++, C# and Rust with a compilation target so that they can run on the web. It is also designed to run alongside JavaScript, allowing both to work together. It also works on the same sandbox as JavaScript. [How to use C++ on the web with Web Assembly.](https://developer.mozilla.org/en-US/docs/WebAssembly/C_to_Wasm)
    - Efficient and fast
    - Fast
    - Open and debuggable (downloadable & executable)
    - Part of the open web platform


    You benefit from .NET performance, reliability and security, use your existing libraries etc. Different components can work together without having to implement an adapter or "middle man".
---
### Blazor
- Blazor Web App option in Visual Studio comes with .NET 8.
- Blazor allows programmers to handle both client and server-side functionality with just C#. Razor is a markup syntax for templates. It incorporates server-side code into the HTML. Blazor, on the other hand, is an SPA (single page app) framework that can run on either Blazor WebAssembly or the Blazor Server, depending on the situation.
- Modern Web Client Landscape → JavaScript / TypeScript on front-end (Angular, React, Vue) or WASM / Blazor / .NET on both front-end and back-end!!
- They don't want to do Angular but they had to do Angular as it was working pretty good with .NET before, but now only Blazor and .NET solve this issue.
- But why not use JavaScript → Because JavaScript might not be the primary expertise of your development team. We can use the same shared code and same actual programming language on client & server with Blazor and .NET. Also, we would be familiar with Tooling, ecosystem and Intellisense.
    - Potential downside → No SCSS/LESS compilation as of now, No JS/TS optimizations such as tree shaking, minification, bundling, lazy loading is cumbersome, PWA support isn't super robust. But these things are currently being worked on.

- Blazor is now component based and focused and embraces the modern web. 
- Blazor uses familiar tech stack (html, css, js/ts), similar data binding models (Vue and React), familiar architecture model, large OSS ecosystem.
- You could modernize a WinForms or WPF app with Blazor, there's a Nuget package that relies on an embedded WebView. (Microsoft.AspNetCore.Components.WebView.WindowsForms/WPF). (Front-end)
- .NET MAUI / .NET MAUI Blazor (Hybrid), succesor of Xamarin, could be use for Mobile. Again, single and shared codebase and it lets you leverage your web skills to build a mobile app. 
-
-