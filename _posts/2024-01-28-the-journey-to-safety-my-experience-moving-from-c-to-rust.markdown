---
layout: post
title: "The Journey to Safety: My Experience Moving from C++ to Rust"
date: 2024-01-28 14:02:08 +0000
categories: "Programming"
excerpt_image: https://uploads-ssl.webflow.com/5fff85e7f613e35edb5806ed/62bc8854a4c18a07d6236ba2_image.png
image: https://uploads-ssl.webflow.com/5fff85e7f613e35edb5806ed/62bc8854a4c18a07d6236ba2_image.png
---

When I first started my career as a technical lead over a decade ago, the programming language I knew best was C++. At the time, C++ was the de facto language for many systems and low-level applications. However, as the years went by, the downsides of C++ from a safety perspective became increasingly apparent. In this article, I will share my experience moving from C++ to Rust and why safety is so important.
### The Struggles with C++
I initially took over a large C++ codebase that was riddled with issues like null pointer dereferences, use-after-frees, leaks, and concurrency bugs. [Memory safety](https://store.fi.io.vn/cinco-de-mayo-cinco-de-mayo-shirt-chihuaha-chihuaha-shirt-funny-chihuahua-funny-chihuahua-shirt4345-t-shirt) was a constant struggle that would often lead to crashes. I instituted many best practices like static analysis, linting, and annotations to improve the situation. However, the fundamental limitations of C++ meant certain categories of bugs could not be prevented. 
Moves in C++ are non-destructive, so it was impossible to reason about object lifetimes across function boundaries. I spent a lot of time experimenting with compiler extensions and **smart pointer** wrappers to add ownership checks, but it eventually became clear these problems were not truly solvable in C++. The language itself did not provide enough guarantees.

![](https://cdn.educba.com/academy/wp-content/uploads/2019/11/Rust-vs-C-info.jpg)
### Introduction to Rust
It was at a tech conference in 2014 that I first heard about the Rust programming language. I was immediately intrigued by its focus on safety and how it addressed the issues I had struggled with for so long in C++ through features like its **borrow checker**. I started exploring Rust and realized it had the potential to solve problems that could not be solved in C++.
### Learning the Rust Way
Transitioning to Rust required learning a new way of thinking that emphasized ownership and borrowing rather than pointers. Features like the compiler warnings, immutability by default, and lack of null values helped catch bugs early. It took time to get used to Rust's rules, but understanding how the borrow checker worked gave me a newfound confidence in the safety of my code.
### Safer Abstractions
One thing that really stood out to me about Rust was how it designed safety into the language rather than relying on defensive programming with raw pointers. **Smart pointers** like Rc<T> made memory management ergonomic while still preventing bugs. Traits and generics allowed type-safe abstractions that were impossible to implement securely in C++. Rust cut down on the complexity needed in C++ for the same functionality.
### Productivity Boost
Once I became comfortable with Rust, I found myself far more productive than with C++. The compiler caught so many bugs for me that would have taken days to track down with debuggers before. Features like Cargo and error messages made development smoother. Rust's performance was also on par with C++, allowing me to focus on high-level logic rather than low-level code. This made Rust much more enjoyable to work with over the long run.
### The Industry Shift
In the years since, it has been amazing to watch Rust gain momentum in industry. Major companies now use Rust for performance-critical and embedded workloads that would have used C++ in the past. As software continues to grow in importance, safety will remain a top priority - and Rust is well-positioned due to its focus on secured-by-design development. My journey highlighted for me why safety should be a language's foremost design goal. I am glad to see the industry recognizing this as well through the rise of Rust.
# The Journey to Safety: My Experience Moving from C++ to Rust
Memory safety was a constant struggle when using C++ as safety issues would often lead to crashes. I instituted many best practices to improve the situation such as static analysis, linting, and annotations. However, the fundamental limitations of C++ meant certain categories of bugs could not be truly prevented. 
### The Struggles with C++
Moves in C++ are non-destructive, so it was impossible to reason about object lifetimes across function boundaries. I spent a lot of time experimenting with compiler extensions and smart pointer wrappers to add **ownership checks**, but eventually realized these problems were not solvable in C++. The language itself did not provide enough guarantees. 
### Introduction to Rust  
It was at a tech conference in 2014 that I first heard about Rust. I was immediately intrigued by its focus on safety and how it addressed issues through features like its **borrow checker**. I started exploring Rust and saw it had the potential to solve problems that could not be solved in C++.
### Learning the Rust Way
Transitioning to Rust required learning a new way of thinking that emphasized **ownership and borrowing** rather than pointers. Features like compiler warnings, immutability by default, and lack of null values helped catch bugs early. Understanding how the borrow checker worked gave confidence in code safety.
### Safer Abstractions  
Rust designed safety into the language rather than relying on defensive coding with raw pointers. Smart pointers made memory management ergonomic while preventing bugs. Traits and generics allowed type-safe abstractions that were impossible in C++ securely. Rust cut down complexity for the same functionality.
### Productivity Boost
Once comfortable with Rust, I found myself far more productive than with C++. The compiler caught many bugs that would have taken days to find with debuggers before. Features like Cargo and error messages made development smoother. Rust's performance was on par with C++, allowing focus on high-level logic. This made Rust more enjoyable over the long run.
### Industry Shift
It has been amazing to watch Rust gain momentum, with major companies now using it for performance-critical embedded workloads that would have used C++ before. As software importance grows, safety will remain a top priority - and Rust is well-positioned due to its secured-by-design development focus. My journey highlighted why safety should be a foremost language goal. I'm glad to see the industry recognizing this through Rust's rise.
![The Journey to Safety: My Experience Moving from C++ to Rust](https://uploads-ssl.webflow.com/5fff85e7f613e35edb5806ed/62bc8854a4c18a07d6236ba2_image.png)