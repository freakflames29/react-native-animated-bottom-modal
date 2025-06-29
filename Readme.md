# 📦 animated-bottom-modal-reactnative

A beautiful and smooth bottom sheet component built using **React Native Reanimated v3** and **Gesture Handler**, designed for easy integration with modal-based workflows.

---

## 🚀 Features

- ⚡ Built with Reanimated 3
- 🧲 Smooth spring/timing animations
- 🪟 Modal-like overlay, easy to integrate into any screen
- 🎨 Customizable background color, height, and border radius
- 🧩 Supports children content
- 🧱 Built-in close button, drag-to-close, and backdrop tap-to-close
- 👆 Drag handle for intuitive gesture-based closing

---

## 📦 Installation

Install this package along with its required peer dependencies:

```bash
npm install animated-bottom-modal-reactnative
```

### 🔗 Peer Dependencies (must be installed in your app):

```bash
npm install react-native-reanimated react-native-gesture-handler
```

> ⚠️ Make sure Reanimated is properly configured according to [the official guide](https://docs.swmansion.com/react-native-reanimated/docs/fundamentals/getting-started).

---

## 🛠️ Usage

```tsx
import React, { useState } from 'react';
import { View, Text, Button } from 'react-native';
import CleanBottomSheet from 'animated-bottom-modal-reactnative';

export default function App() {
  const [visible, setVisible] = useState(false);

  return (
    <View style={{ flex: 1 }}>
      <Button title="Open Bottom Sheet" onPress={() => setVisible(true)} />

      <CleanBottomSheet
        visible={visible}
        onClose={() => setVisible(false)}
        height={500}
        backgroundColor="#fff"
        borderRadius={30}
        showCross={true}
      >
        <View style={{ padding: 20 }}>
          <Text style={{ fontSize: 18 }}>This is the content of the sheet</Text>
        </View>
      </CleanBottomSheet>
    </View>
  );
}
```

---

## ✨ Props

| Prop           | Type               | Default   | Description                                                      |
| -------------- | ------------------ | --------- | ---------------------------------------------------------------- |
| `visible`      | `boolean`          | `false`   | Controls the visibility of the bottom sheet                      |
| `onClose`      | `() => void`       | `-`       | Function to call when closing the bottom sheet                   |
| `height`       | `number`           | `600`     | Height of the bottom sheet                                       |
| `backgroundColor` | `string`        | `#fff`    | Background color of the sheet container                          |
| `borderRadius` | `number`           | `30`      | Border radius for the top corners of the sheet                   |
| `children`     | `React.ReactNode`  | `-`       | Custom content to show inside the bottom sheet                   |
| `showCross`    | `boolean`          | `true`    | Whether to show the close (cross) button                        |

---

## 📷 Screenshot

<img src="https://raw.githubusercontent.com/freakflames29/react-native-animated-bottom-modal/refs/heads/main/android.png" alt="Android" width="350">
<img src="https://raw.githubusercontent.com/freakflames29/react-native-animated-bottom-modal/refs/heads/main/ios.png" alt="Android" width="350">

---

## 📌 Notes

* This component renders as an absolutely positioned overlay, so you can use it anywhere in your component tree.
* The close button uses a static image: `close.png`. You may need to replace it with your own icon/image or customize it further.
* Supports drag-to-close gesture and tap on backdrop to close.

---

## 🤝 Contributing

Pull requests and feedback are welcome! If you find bugs or want features, feel free to open an issue.

---

## 👤 Author

Made with ❤️ by [Sourav Das](https://github.com/freakflames29)
