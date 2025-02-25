# 🤖 Just A Few ... "General" System Prompts
 
![LLM](https://img.shields.io/badge/LLM-blue)
![Prompt Engineering](https://img.shields.io/badge/Prompt_Engineering-green)

Here is a quandary that those who work with LLMs via API through self-hosted chat interfaces (etc) are familiar with:

- Without any system prompt at all (at least one visible to the user), the default model behavior feels a little bit flat and lifeless.
- With a deterministic system prompt, a model effectively becomes an "assistant" (and with context and API actions, a full-fledged agent).   

I haven't found a word yet for the kind of light touch configurations that are intended to configure LLM APIs to act as "general purpose" tools ... think the kind of (mostly) neutral experiences provided by interfaces like ChatGPT (etc).

We all know intuitively what these behaviors feel like (for better and for worse). But nailing them down with good general purpose system prompts is, like much in prompt engineering, more art than science. 

This repo will contain a very small selection of general system prompts as I keep them on hand and iterate through them to try to have a general purpose model or two in my collection. 

As templates, I'll also add any publicly accesible ones from major platforms that I can find to serve as guidelines of sorts. [Anthropic](https://docs.anthropic.com/en/release-notes/system-prompts#feb-24th-2025) open-sources their system prompts!

## 🗺️ Specific Parts Of This Repo

- 🏢 `vendor-models` Contains system prompts that are based upon those of real major vendor models, stripped of some brand references and guardrails. 
- 🎯 `system-prompts/` The core directory containing various prompt configurations:
  - 🎭 `model-personalities/` Defines different AI personality traits:
    - Standard personalities: brusque, creative, empathetic, encouraging, flamboyant, formal, ideator
    - `slightly-deviant/` Contains more unique personality configurations
  - ⛔ `negative-prompts/` Contains prompts defining what the model should not do
  - 🌍 `user-geolocation/` Geographic-specific configurations (e.g., American, Israeli)
  - 👤 `user-personality/` Tailored prompts for different user types (philosophers, tech people, etc.)
  - 🌈 `user-worldview/` Prompts reflecting different philosophical perspectives (optimists, realists)

- 🛠️ `build-assistants/` Contains tools for prompt configuration:
  - ⚡ `create-meta-configs/` Features a powerful meta-configuration system that:
    - Acts as a prompt builder combining different stylistic elements
    - Allows creating generalist system prompts by combining:
      - 🎨 User personality traits
      - 🗳️ User political views
      - 📍 User geolocation
      - 🤖 Model personality preferences
    - Example use: "Create a system prompt for an Israeli user with an optimistic personality who prefers enthusiastic AI interactions"
  - 📝 `create-individual-configs/` For building standalone configurations

- `by-vendors/` Contains reference prompts from major vendors:
  - `anthropic/` Includes Anthropic's open-sourced system prompts

## Repository Structure Highlights

1. **Modular Design**: The repository uses a modular approach where different aspects of system prompts are separated into distinct categories
2. **Meta Configuration**: The meta system prompt assistant (`build-assistants/create-meta-configs/`) serves as a powerful tool for combining different prompt elements into cohesive configurations
3. **Personality Matrix**: Extensive collection of both model and user personality configurations
4. **Geographic Awareness**: Includes geolocation-specific prompts for different user bases
5. **Vendor References**: Maintains reference implementations from major vendors for benchmarking

## Third Person Or Second Person?

An open ended question which I do not have the answer to but have always wondered (if you know the answer, drop me a line!): should system prompts be written in the second or third person.

I.e., 

"You are Claude, a witty assistant."

or:

"The model is Claude, a witty assistant."

I tend naturally towards writing system prompts in the second person so as to instruct the model. But as I learned more about best practices and through my own experimentation, I may change tact. 

## Author

Daniel Rosehill  
(public at danielrosehill dot com)

## Licensing

This repository is licensed under CC-BY-4.0 (Attribution 4.0 International) 
[License](https://creativecommons.org/licenses/by/4.0/)

### Summary of the License
The Creative Commons Attribution 4.0 International (CC BY 4.0) license allows others to:
- **Share**: Copy and redistribute the material in any medium or format.
- **Adapt**: Remix, transform, and build upon the material for any purpose, even commercially.

The licensor cannot revoke these freedoms as long as you follow the license terms.

#### License Terms
- **Attribution**: You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **No additional restrictions**: You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

For the full legal code, please visit the [Creative Commons website](https://creativecommons.org/licenses/by/4.0/legalcode).