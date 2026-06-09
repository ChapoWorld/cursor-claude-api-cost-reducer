# 🚀 Cursor AI: Reduce Claude API Costs by 90%

If you are using Cursor AI (or VSCode with Roo Code/Cline) with the official Anthropic Claude API, you have probably noticed how quickly it burns through your API balance. 

This repository provides a configuration guide on how to utilize **Enterprise AWS Vertex AI Prompt Caching** to reduce your Claude Opus 4.8 and Sonnet 4.6 API costs by up to 90%.

## 💡 The Problem: Standard Anthropic API
Standard API keys charge you full price for every single token sent in the context window. When working on large codebases in Cursor, you are constantly re-sending the same context, resulting in massive bills.

## ✅ The Solution: Active Prompt Caching
By switching to a cached endpoint, you only pay for *new* inputs and outputs. Your old context is processed almost for free (80-95% cache hit rate).

**Example of savings:**
* Cost of project with standard tokens: `$800.00`
* Cost of same project with Cached Endpoint: `~$98.00` (8X reduction)

## 🛠️ How to Setup in Cursor

1. **Get a Cached Enterprise API Key & Endpoint:**
   To make this work, you need a custom Base URL that supports Enterprise Vertex AI pooling. You can get a pre-configured, high-limit key here:
   👉 **[Get Enterprise Claude API Key (Instant Delivery)](https://claude.sell.app/product/claude-api-tokens)**

2. **Configure Cursor:**
   * Open Cursor Settings -> `Models`
   * Under `OpenAI API Key` or `Anthropic API Key`, paste your new unique API Key.
   * Toggle `Override OpenAI Base URL` (or Anthropic Base URL).
   * Paste the Custom Base URL provided with your purchase.
   * Save and start coding!

## 🤖 Supported Models
This endpoint override works natively with:
* `claude-3-5-sonnet-20241022` (Thinking 1M)
* `claude-3-opus-20240229`
* `claude-3-5-haiku-20241022`

Stop overpaying for your AI coding assistant!
