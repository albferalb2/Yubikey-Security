# 🔐 YubiKey Custom ID Registrar

A local tool powered by WebAuthn to register multiple security keys (like YubiKey, SoloKey, etc.) with a custom user-defined identifier. It runs **entirely in the browser**, with no need for internet or backend services.

## 🧩 Features

- Register physical security keys using the WebAuthn API.
- Assign a custom name or ID to each key.
- Detect and prevent duplicate `credentialId`s.
- Store data locally using browser `localStorage`.
- Simple UI to view and delete registered keys.

## 🖥️ Requirements

- A modern browser (Chrome, Firefox, Edge).
- A WebAuthn-compatible security key (e.g., YubiKey).
- A **local web server** is required due to WebAuthn security restrictions (see below).

## 🚀 Local Usage

> **Important**: WebAuthn only works on secure origins. It will **not** work if you open the file directly (`file://`). You must serve it from `http://localhost`.

### Option 1: Node.js + `npx serve`

```bash
npx serve .
