# Modern Systems Programming 🦀

[//]: # ([![Build workflow]&#40;https://img.shields.io/github/actions/workflow/status/google/comprehensive-rust/build.yml?style=flat-square&#41;]&#40;https://github.com/google/comprehensive-rust/actions/workflows/build.yml?query=branch%3Amain&#41;)

[//]: # ([![GitHub contributors]&#40;https://img.shields.io/github/contributors/google/comprehensive-rust?style=flat-square&#41;]&#40;https://github.com/google/comprehensive-rust/graphs/contributors&#41;)

[//]: # ([![GitHub stars]&#40;https://img.shields.io/github/stars/google/comprehensive-rust?style=flat-square&#41;]&#40;https://github.com/google/comprehensive-rust/stargazers&#41;)

This is a modified course from [Comprehensive Rust 🦀](https://google.github.io/comprehensive-rust/),
a free Rust course developed by the Android team at Google. The course
covers the full spectrum of Rust, from basic syntax to advanced topics like
generics and error handling.

[//]: # (> The latest version of the course can be found at)

[//]: # (> <https://google.github.io/comprehensive-rust/>. If you are reading somewhere)

[//]: # (> else, please check there for updates.)

[//]: # (>)

[//]: # (> The course is available in other languages. Select your preferred language in)

[//]: # (> the top right corner of the page or check the)

[//]: # (> [Translations]&#40;running-the-course/translations.md&#41; page for a list of all)

[//]: # (> available translations.)

[//]: # (>)

[//]: # (> The course is also available [as a PDF]&#40;comprehensive-rust.pdf&#41;.)

The goal of the course is to teach you Rust and its relevant to systems programming. We assume you don't know anything
about Rust and hope to:

- Give you a comprehensive understanding of the Rust syntax and language.
- Enable you to modify existing programs and write new programs in Rust.
- Show you common Rust idioms.

We call the first four course days Rust Fundamentals.

Building on this, you're invited to dive into one or more specialized topics:

[//]: # (- [Android]&#40;android.md&#41;: a half-day course on using Rust for Android platform)

[//]: # (  development &#40;AOSP&#41;. This includes interoperability with C, C++, and Java.)

[//]: # (- [Chromium]&#40;chromium.md&#41;: a half-day course on using Rust within Chromium based)

[//]: # (  browsers. This includes interoperability with C++ and how to include)

[//]: # (  third-party crates in Chromium.)
- [Bare-metal](bare-metal.md): a whole-day class on using Rust for bare-metal
  (embedded) development. Both microcontrollers and application processors are
  covered.
- [Concurrency](concurrency/welcome.md): a whole-day class on concurrency in
  Rust. We cover both classical concurrency (preemptively scheduling using
  threads and mutexes) and async/await concurrency (cooperative multitasking
  using futures).

Rust is currently used in many performance-critical applications, from system programming to machine learning and AI.
PLease feel free to take a look at these projects for some ideas about where Rust is being used:
- [Tokio](https://tokio.rs/): Asynchronous runtime for I/O, networking, scheduling, timers, ...
- [Rust for Linux](https://rust-for-linux.com/): is the project adding support for the Rust language to the Linux kernel
- [Quiche](https://github.com/cloudflare/quiche): powers Cloudflare edge HTTP/3 and QUIC transport protocol
- [Candle](https://github.com/huggingface/candle): Minimalist ML framework for Rust (inference-focused)
- [Burn](https://burn.dev/): Comprehensive Deep Learning framework in Rust
- [Rust OSDev](https://github.com/rust-osdev): Tools & libraries for OS development in Rust
- [Writing an OS in Rust](https://os.phil-opp.com/): A tutorial for creating a small OS in Rust
- [Cloud-hypervisor](https://github.com/cloud-hypervisor/cloud-hypervisor), [Alioth](https://github.com/google/alioth): Virtual machine monitors
- [Rust and WebAssembly](https://rustwasm.github.io/docs/book/): building Rust application for [WebAssembly](https://webassembly.org/) virtual machine  

## Non-Goals

Rust is a large language and we won't be able to cover all of it in a few days.
Some non-goals of this course are:

- Learning how to develop macros: please see
  [Chapter 19.5 in the Rust Book](https://doc.rust-lang.org/book/ch19-06-macros.html)
  and [Rust by Example](https://doc.rust-lang.org/rust-by-example/macros.html)
  instead.

## Assumptions

The course assumes that you already know how to program. Rust is a
statically-typed language and we will sometimes make comparisons with C and C++
to better explain or contrast the Rust approach.

If you know how to program in a dynamically-typed language such as Python or
JavaScript, then you will be able to follow along just fine too.

<details>

This is an example of a _speaker note_. We will use these to add additional
information to the slides. This could be key points which the instructor should
cover as well as answers to typical questions which come up in class.

</details>
