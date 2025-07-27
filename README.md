# Homebridge August Locks (jstroins fork)

This is a **fixed and updated fork** of the [original Homebridge August Locks plugin](https://github.com/nnance/homebridge-august-locks), which integrates [August Smart Locks](https://august.com) with [Homebridge](https://homebridge.io), allowing you to control your locks via Apple HomeKit.

This version includes bug fixes, updated JSON parsing, and improved stability for modern August API responses.

---

## 🔧 Features

- Lock and unlock your August Smart Lock from HomeKit
- Monitor lock status and events
- Uses August Cloud API via your August account credentials
- Compatible with August Connect Bridge

---

## 🚀 Installation

### From GitHub (recommended for now)

```bash
sudo npm install -g https://github.com/jstroins/homebridge-august-locks.git
```

After installation, restart Homebridge.

---

## ⚙️ Configuration

Add this to your Homebridge `config.json`:

```json
{
  "platform": "AugustLocks",
  "name": "August Locks",
  "username": "your@email.com",
  "password": "your-password",
  "installId": "a-random-uuid",
  "augustApiKey": "api-key-if-required",
  "code": "123456",         // (Optional) 2FA code
  "mfaType": "phone"        // (Optional) "phone" or "email"
}
```

> You can generate a random `installId` using the command `uuidgen`.

If 2FA is enabled, use the August app first to approve the login attempt, or set `code` and `mfaType` in the config.

---

## 🛠 Fixes in This Fork

- ✅ Fixed broken JSON parsing for multi-chunk API responses
- ✅ Added better debug logging and error handling
- ✅ Ensured compatibility with modern Node.js and Homebridge versions
- ✅ Cleaned up the plugin for long-term maintenance

---

## 🙋‍♂️ Author

This fork is maintained by [Jakub Stroinski](https://github.com/jstroins) ([@jstroins](https://github.com/jstroins)).

If you find this plugin useful, feel free to [star the repo](https://github.com/jstroins/homebridge-august-locks) or open issues/pull requests if you’d like to contribute.

---

## 📝 License

MIT — feel free to use, modify, and share.