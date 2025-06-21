
# 📦 animated-bottom-modal-reactnative


A beautiful and smooth bottom sheet component built using **React Native Reanimated v3** and **Gesture Handler**, designed for easy integration with modal-based workflows.

---

## 🚀 Features

- ⚡ Built with Reanimated 3
- 🧲 Smooth spring/timing animations
- 🪟 Uses `Modal` API — easy to integrate into any screen
- 🎨 Customizable background color and height
- 🧩 Supports children content
- 🧱 Built-in close button and backdrop tap-to-close

---

## 📦 Installation

Install this package along with its required peer dependencies:

```bash
npm install animated-bottom-modal-reactnative
````

### 🔗 Peer Dependencies (must be installed in your app):

```bash
npm install react-native-reanimated react-native-gesture-handler
```

> ⚠️ Make sure Reanimated is properly configured according to [the official guide](https://docs.swmansion.com/react-native-reanimated/docs/fundamentals/installation/).

---

## 🛠️ Usage

```tsx
import React, { useState } from 'react';
import { View, Text, Button } from 'react-native';
import { BottomSheet } from 'animated-bottom-modal-reactnative';

export default function App() {
  const [visible, setVisible] = useState(false);

  return (
    <View style={{ flex: 1 }}>
      <Button title="Open Bottom Sheet" onPress={() => setVisible(true)} />

      <BottomSheet
        visible={visible}
        onClose={() => setVisible(false)}
        height={500}
        backgroundColor="#fff"
      >
        <View style={{ padding: 20 }}>
          <Text style={{ fontSize: 18 }}>This is the content of the sheet</Text>
        </View>
      </BottomSheet>
    </View>
  );
}
```

---

## ✨ Props

| Prop              | Type              | Default     | Description                                    |
| ----------------- | ----------------- | ----------- | ---------------------------------------------- |
| `visible`         | `boolean`         | `false`     | Controls the visibility of the modal           |
| `onClose`         | `() => void`      | `undefined` | Function to call when closing the modal        |
| `height`          | `number`          | `600`       | Height of the bottom sheet                     |
| `backgroundColor` | `string`          | `#471396`   | Background color of the sheet container        |
| `children`        | `React.ReactNode` | `-`         | Custom content to show inside the bottom sheet |

---

## 📷 Screenshot

<img src="https://raw.githubusercontent.com/freakflames29/react-native-animated-bottom-modal/refs/heads/main/android.png" alt="Android" width="350">
<img src="https://raw.githubusercontent.com/freakflames29/react-native-animated-bottom-modal/refs/heads/main/ios.png" alt="Android" width="350">


---

## 📌 Notes

* This component uses `Modal` under the hood, so it's safe to use anywhere in the component tree.
* The close button uses a static image: `close.png`. You may need to replace it with your own icon/image or customize it further.

---


## 🤝 Contributing

Pull requests and feedback are welcome! If you find bugs or want features, feel free to open an issue.

---

## 👤 Author

Made with ❤️ by [Sourav Das](https://github.com/freakflames29)
