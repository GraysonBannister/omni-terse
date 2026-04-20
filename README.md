# Omni Terse

An [Omni Code](https://github.com/GraysonBannister/omni-code) add-on that reduces output token usage by injecting a terse-output system prompt fragment. Works with all LLM providers — Claude, GPT-4, Gemini, Grok, Mistral, and more.

## How It Works

Registers a system prompt fragment that instructs the model to respond concisely, eliminating the preamble, filler, and padding that inflate output token counts without adding information.

Inspired by the [Caveman](https://github.com/juliusbrussee/caveman) token optimization technique.

**Estimated savings: ~40–75% output token reduction**

## What Gets Removed

- **Preambles**: "I'll now...", "Let me...", "Sure!", "Great question!", "Of course!"
- **Summaries**: "I've completed...", "In summary...", "To recap..."
- **Transition padding**: "First, I'll...", "Next, I'll...", "Finally, I'll..."
- **Hedging**: "I think", "It seems", "You might want to" where confidence is warranted
- **Obvious code comments** that only restate what the code does

## What Gets Kept

All actual information, reasoning, and code output is preserved. The addon only removes content that adds length without adding value.

## Usage

Install the addon, and it activates automatically. No configuration required. Every conversation will use the terse output style from that point on.

To disable, uninstall or disable the addon in the Omni Code Add-ons panel.

## Requirements

- Omni Code v2.0.0 or later

## Installation

Install via the Omni Code Add-ons panel or directly from the [registry](https://graysonbannister.github.io/omni-code-website/addons).

## License

MIT
