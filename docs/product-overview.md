# Clip Text — product and partnership brief

- **Working name:** Clip Text
- **Platform:** Windows 10/11
- **Audience:** Comic artists, illustrators, and writers using CLIP STUDIO PAINT
- **Stage:** Early desktop prototype; commercial launch pending

## Product

Creators frequently need to correct Korean spelling and spacing, refine dialogue, or translate a text layer. Clip Text is designed to keep that work close to the canvas, reducing the need to move text between an editor and a separate AI interface.

While editing text, the user appends `ㅁ` for correction or `ㅂ` for translation and presses Ctrl + Hanja. The application is designed to remove the command character and replace the text after a completed request. A home screen also lets the user enter text directly and review results.

Preferences include editing strength (low, medium, high, or automatic), writing style (spoken, written, or automatic), and translation target language. There is no bundled local language model.

## Current development

The desktop prototype includes home and settings screens, Korean and English interface labels, command parsing, background processing, a Windows keyboard hook and clipboard controller, and system tray controls. The replacement controller rechecks the source and editing focus before pasting, and cancels when those change.

Automated tests for commands, settings, simulated clipboard transactions, and UI behavior pass. The [screenshots](../README.md#prototype-screens) were captured from the running application using an offscreen Qt renderer on Linux. Their sample input was not sent to an AI service.

Actual Windows keyboard/IME behavior and CLIP STUDIO PAINT text replacement still require end-to-end testing. Live model quality has not been validated. Sign in with ChatGPT and ChatGPT plan usage are not yet enabled.

## Requested ChatGPT integration

We are requesting **both Sign in with ChatGPT and ChatGPT plan use for eligible AI requests** for a commercial desktop application. Each user would authenticate their own account and explicitly authorize plan usage. The application does not need access to ChatGPT conversation history or memories.

We intend to follow the approved commercial integration with an issued client ID, supported callback URLs, and eligible models. Account connection, token handling, usage-limit behavior, and branding will be implemented and validated under the approved integration requirements before release.

Commercial approval has not been received. The application does not currently claim to be an OpenAI partner. The relevant [developer documentation](https://developers.openai.com/siwc) and [commercial interest form](https://openai.com/form/sign-in-with-chatgpt-interest/) provide the intended application route.

## Commercial plan

The intended product is a paid desktop application for individual creators. Pricing, the licensing model, and the release date are not yet finalized. The app fee would be separate from the user's ChatGPT subscription, and eligible requests would count toward that user's authorized ChatGPT plan allowance.

The next development milestones are commercial integration approval, account connection, live request validation, Windows/CLIP STUDIO PAINT testing, and preparation of a distributable Windows package.
