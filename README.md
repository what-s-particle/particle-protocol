# What

This repository is used to build the `Particle framework`, and it defines using the [Protocol Buffers](https://protobuf.dev/).

# Why

The protocol definition will not be affected by the business and the coding language of the implementation.
So separate it into a repository, please note that this is a repository containing only `.proto` files, we do not provide scripts to generate corresponding languages.

BUT: Considering that the defined  `.proto` files can be quickly used by the caller(backend, web, mobile), we provide a script(`gennerate.py`) that will merge all `*.proto` into one file.
I'll come back to the reason for this, I did do some research and this is the best solution I can think of for quickly generating code for a variety of languages.

# How

The protocol files have a clear directory structure. If you observe it carefully, it will be easy to get started with adding and modifying protocol files.
As mentioned above, the end integrating this protocol needs to clone this repository to the latest, and refer to the provided script to generate the corresponding programming language file.

# Addition

Please note that if you use IDEA to open this project, you need to install the `protocol buffer` plug-in and configure some `source file path`s to ensure that the IDE can successfully recognize and support import jumps, which is very useful for you to modify this warehouse.
You can easily find the answer on the Internet, I won't repeat it.

# About Particle Modeling

## Abstract an application page

Ensuring the stability of the abstraction level of the page is a key to the success of a Server-Driven UI framework. Particle defines the following three parts, attempting to establish a page data model that is both user-friendly, maintainable, and extensible.

Page structure: The page structure is the layout relationship between the various components of the page. For a page, it can be divided into several areas, each of which contains several page elements. Different areas can use different layout methods, such as vertical layout, horizontal layout, or grid layout.

Page elements: Page elements are the visible parts of the page, including text, images, buttons, forms, lists, etc. Each element has its own properties and styles, such as font, color, size, background, etc.

Page interactions: Page interactions generally refer to various `operations` and `feedback` that users perform on the page. `Operations` include clicking, sliding, inputting, zooming, rotating, etc., and `feedback` includes invisible form submissions, state changes on the page, permission request prompts, and animations, etc.

This is a very common abstract model in front-end development, used to describe the composition, style, and interactive behavior of a page. It can be applied in different front-end frameworks and development tools, such as `React`, `Vue`, `Angular`, `SwiftUI`, `Compose`, etc.

Regarding the `operations` part of page interaction, it should also include some non-user behaviors. For example, in the scenario where "when the `Home` page of the application is first displayed on the screen, a loading prompt box pops up," we can understand `first displayed on the screen` as an operation, and `popping up the loading prompt box` as its feedback. In view of this, we collectively refer to all operations as `Events`.
