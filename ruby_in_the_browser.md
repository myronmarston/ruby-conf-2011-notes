## Ruby in the browser

* HTML 5 is awesome, but it's forcing a monoculture: JS is the only way to do it.
* JavaScript as a manopoly? they (ECMA) are colluding against us...
  * All the major vendors have agreed to make all of us use the same language
* Diversity is good...experimentation leads to innovation
* 50+ ruby implementations
* We have coffeescript in browser now...why not ruby, too?
* Not just about ruby in the browser...ruby/python/x/y/z in the browser.
* Gestalt: by the Microsoft Team. Ruby & Python in the browser.
  * MS Silverlight + DLR
* Is there a future for Silverlight and IronRuby?
* Browser plugins: a brief detour
  * Adobe got PDFs to work in Netscape by reverse-engineering Netscape
  * Gave birth to NPAPI (netscape plugin API)
    * in use by most browsers to this day
    * plugin registers a content-type (i.e. `music/mp3`)
    * Browser encouters the ile, delegates to plugin
  * ...but this is a security nightmare
  * Google Chrome: WebKit, V8, NaCl, Speed...
    * As of Sept, 2011, Chrome has 26% marketshare; will soon be #2.
    * Every tab is an isolated process w/ security sandbox
    * They have PPAPI (Pepper) (NaCl--native client--is "salt")
      * Sandboxing technology for safe execution of native code
      * Native machine code runs on the client CPU
      * Not an interpreter
      * Uses modified GCC compiler
      * Must build for different CPU architectures
      * NaCl runtime verifies untrusted code (static analysis)
      * NaCl executed verified code
      * No fork, process control, file system access, etc
* NaCL provides JS callbacks for native communication
* Embed with embed tag
* Has an NaCl SDK/API
* You have the same privileges as JS runtime
* NaCl ports--ports of many C/C++ libraries
* You need Chrome 9 with NaCl enabled
* Quake in the browser.
* Future of NaCl?
  * It's a built-in plugin in chrome
  * PNaCl will replace NaCl in 2012
  * Enable NaCl in about:plugins
  * Google app engine is using on the server for a sandbox
  * Exacycle: 1 billion CPU hours for research; uses NaCl
* PNaCl: toolchain for LLVM bitcode. Runs LLVM bitcode in browser.
  * Will enable dozens of languages
* EMScripten: LLVM to JS compiler
* emscripted-ruby: ruby 1.8.7 that compiles to JS
* Check out repl.it: llvm in your browser
