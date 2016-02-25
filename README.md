# laf-optimizer

Look-and-Feel optimizer for Swing: i.e., "get that Metal out of here."

It basically tries to use your native OS look-and-feel, unless that's Metal, too. If it is, it just disables a bunch of bold stuff so it looks *less* ugly.

## Usage

In your `SwingUtilities.invokeLater` call that starts your application, add a call to `LAFOptimizer.optimizeSwing()` before you instantiate any Swing components. That is, it should be the first statement in your callback.

If there are other things before the call to `optimizeSwing`, you may get inconsistent styling.

## Demo

Here's a demo with some random components. This is running on Linux, and I've included a native app in the background for comparison.

Before:
![Unoptimized Swing components demo](https://cloud.githubusercontent.com/assets/4317806/13331089/f365b51e-dbc9-11e5-9f9b-303efc124674.png)

After:
![Optimized Swing components demo](https://cloud.githubusercontent.com/assets/4317806/13331088/f365af60-dbc9-11e5-8e91-3c66b74f5e17.png)

The only change is a call to `LAFOptimizer.optimizeSwing()`.

## License

MIT
