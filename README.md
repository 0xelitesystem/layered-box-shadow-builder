# Layered Box Shadow Builder

Visual CSS box-shadow builder with live preview, stacked layers, inset support, and copy-ready output.

**Live demo:** https://0xelitesystem.github.io/layered-box-shadow-builder/

## Use

1. Open the tool. A default two-layer shadow is already applied to the preview box.
2. Drag the sliders (or type exact numbers) for offset X, offset Y, blur, spread, and opacity on each layer.
3. Pick a color per layer and toggle **inset** for inner shadows.
4. Stack more than one shadow with **Add layer**. Reorder layers with **Up** and **Down** (the top layer paints in front), or **Copy** and **Remove** them.
5. Start from a **preset** (Subtle, Medium, Large, Floating, Glow, Inset, Neumorphic) and adjust from there.
6. Tune the preview box size, corner radius, box color, and backdrop color under **Preview settings** to check the shadow against a realistic surface.
7. Read the generated CSS in the code block and hit **Copy CSS** for the full declaration, or **Copy value only** for just the value.

Already have a value? Paste it into **Import from CSS** and choose **Parse and load** (replace) or **Parse and append**. The parser understands multiple comma-separated shadows, `inset`, and any valid CSS color (hex, `rgb()`, `rgba()`, `hsl()`, and named colors). Invalid input is reported per shadow instead of failing silently. Your work is saved in the browser and restored on your next visit.

## Why this exists

Most box-shadow builders are wrapped in ad scripts, analytics, and third-party trackers, and many quietly break on multi-layer or inset shadows. This one is a single HTML file with no dependencies, no build step, no network calls, and no surveillance. It implements the real CSS `box-shadow` grammar, so what you preview is exactly what you copy. It is MIT licensed, so you can read every line, fork it, or self-host it.

## Privacy

Everything runs in your browser. There is no server, no analytics, no telemetry, and no network request of any kind. The only data stored is your current shadow, kept in this site's `localStorage` on your own machine so the tool remembers your work between visits. Nothing ever leaves your device. Clear the value any time with your browser's site-data controls.

## Run locally

Clone the repository and open the file directly:

```
git clone https://github.com/0xelitesystem/layered-box-shadow-builder.git
cd layered-box-shadow-builder
```

Then open `index.html` in any browser. To serve it over HTTP instead (which enables the one-click clipboard copy in more browsers):

```
python -m http.server
```

Then visit `http://localhost:8000`.

## Build

No build. No bundler, no dependencies, no toolchain. It is one self-contained `index.html` with inline CSS and JavaScript. Edit the file and refresh.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. See [LICENSE](LICENSE).

## Related

- [wcag-contrast-ratio-check](https://github.com/0xelitesystem/wcag-contrast-ratio-check)
- [css-gradient-composer](https://github.com/0xelitesystem/css-gradient-composer)
- [jwt-inspector](https://github.com/0xelitesystem/jwt-inspector)
