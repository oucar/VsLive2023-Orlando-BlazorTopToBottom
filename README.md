### VSM01 - Workshop: Blazor Top to Bottom
- JavaScript was the only language that could run on the web some while ago, but now it's possible with C#, or more specifically Blazor.
- **Polyglot Programming**: Polyglot programming is the practice of writing code in multiple languages to capture additional functionality and efficiency not available in a single language. 
- Dependency Injection
    - Blazor is built on top of dependency injection.
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
- For back-end, it lets you leverage the stability an consistency of .NET. Lets you run apps outside the browser, it also lets you compile apps to .wasm and run on any host. So it doesn't really make a huge difference if you're just an API or heavily back-end focused developer, but at least it would make a better sense for a back-end developer when they look into a front-end implementation of a component. 
- For Client & Server → Single-stack development. It's pretty popular in other languages (MEAN, MERN). 
- Everything in Blazor is called Razor Component (cshtml), but now its `Abc.razor`. This is to differentiate the old Razor and Blazor Razor. Each .razor file is essentialy been compiled into a C# class.
- Some old razor compoenents are also built into Blazor. Compoenents work just like the components in React, Vue, etc. They work independently. Components can take `[Parameters]` that work like the props in React, meaning that same components can work in different ways in different pages.
- Cascading Parameters: Blazor comes with a special component called CascadingValue. This component allows whatever value is passed to it to be cascaded down its component tree to all of its descendants. The descendant components can then choose to collect the value by declaring a property of the same type, decorated with the [CascadingParameter] attribute.
- Right click into a XXXXX and hit "turn into code behind (?)", then it generates the C# class that Blazor turns .razor file into C#.
- Blazor doesn't use MVC, it uses MVvM (list differences). 
    - [MVC & MVVM](https://medium.com/@ankit.sinhal/mvc-mvp-and-mvvm-design-pattern-6e169567bbad)
    - MVVM lets you pull out the business logic from the page related logic, like the click events etc.
- Blarzorise - Robust UI component library tailored for Blazor [Documentation](https://blazorise.com/docs/components/)

---
### Blazor WASM Project Setup (EngineAnalyticsWebApp)
- App Type: Blazor WebAssemly Standalone App 
- Best practice is to isolate components such as client and server. (UI, Components, Shared for this example)
- In modern web components, there should be modern web data-binding, reusability and cohesive chunks of functionality. 
- Run the app first the and the second time, show metrics in Network tab in developer console.
- Web assemblies are unique to the application, it runs once for an application then those are being saved in the cache of the website.
- Lazy Loading: Assets will not load until portion of app navigated to by user, it load assemblies ad-hoc to improve performance. 
- It's also possible to call JavaScript from Blazor, and vice versa. 
- PWA: Web application that can like an application on your machine that also can work offline. Blazor lets you do that as well.

---
### 