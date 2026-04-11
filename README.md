[![crates.io](https://img.shields.io/crates/v/egui-screensaver-mystify.svg)](https://crates.io/crates/egui-screensaver-mystify)
[![docs.rs](https://docs.rs/egui-screensaver-mystify/badge.svg)](https://docs.rs/egui-screensaver-mystify)
[![Rust version](https://img.shields.io/badge/rust-1.85%2B-orange.svg)](https://www.rust-lang.org)
[![License: MIT OR Apache-2.0](https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-blue.svg)](LICENSE-MIT)
[![dependency status](https://deps.rs/repo/github/cecton/egui-screensaver-mystify/status.svg)](https://deps.rs/repo/github/cecton/egui-screensaver-mystify)
[![CI](https://github.com/cecton/egui-screensaver-mystify/actions/workflows/ci.yml/badge.svg)](https://github.com/cecton/egui-screensaver-mystify/actions/workflows/ci.yml)
[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://cecton.github.io/egui-screensaver-mystify/)

# egui-screensaver-mystify

Mystify screensaver for [egui](https://github.com/emilk/egui).

Renders two bouncing quadrilaterals with colour-cycling trails onto the egui
background layer, recreating the classic Windows 3.x Mystify screen saver.

## Usage

Add the crate to your `Cargo.toml`:

```toml
[dependencies]
egui-screensaver-mystify = "0.1"
```

Then call `paint` every frame from your `eframe::App::update` implementation,
before drawing any UI windows:

```rust
use egui_screensaver_mystify::MystifyBackground;

struct MyApp {
    mystify: MystifyBackground,
}

impl eframe::App for MyApp {
    fn update(&mut self, ctx: &egui::Context, _frame: &mut eframe::Frame) {
        self.mystify.paint(ctx);
        // … rest of your UI …
    }
}
```

## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE))
- MIT License ([LICENSE-MIT](LICENSE-MIT))

at your option.
