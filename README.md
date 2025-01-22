# RDCircleProgressKit

![GitHub repo size](https://img.shields.io/github/repo-size/divyesh-pansuriya/RDCircleProgressKit)
![GitHub stars](https://img.shields.io/github/stars/divyesh-pansuriya/RDCircleProgressKit?style=social)
![GitHub forks](https://img.shields.io/github/forks/divyesh-pansuriya/RDCircleProgressKit?style=social)

**RDCircleProgressKit** is a lightweight and highly customizable circular progress view designed for iOS applications. It allows you to create visually appealing progress indicators with optional center images, making it perfect for dashboards, fitness apps, and more.  

This library is implemented as a single Swift file, making integration into your project seamless and hassle-free.

---

### Screenshots

<table>
  <tr>
    <td><img src="Images/Screenshot - 1.png" width=270></td>
    <td><img src="Images/Screenshot - 2.png" width=270></td>
    <td><img src="Images/Screenshot - 3.png" width=270></td>
  </tr>
  <tr>
    <td><img src="Images/Screenshot - 4.png" width=270></td>
    <td><img src="Images/Screenshot - 5.png" width=270></td>
    <td><img src="Images/Screenshot - 6.png" width=270></td>
  </tr>
</table>

---

## **Key Features**

- Smooth circular progress visualization with adjustable **colors** and **line width**.
- Configurable for **clockwise** or **counterclockwise** progress animation.
- Optional **center image** support with customizable insets and scaling modes.
- Lightweight and easy to integrate.
- Fully customizable via **code** or **Interface Builder**.
- Support for animations to update progress dynamically.

---

## **Installation**

### **Manual Setup**

1. Clone or download this repository.
2. Copy the `RDCircleProgressView.swift` file into your project directory.
3. Ensure the file is added to your app’s target in **Build Phases**.

---

## **Usage**

### **Programmatically**

To create and customize a `RDCircleProgressView` instance:  

```swift
import UIKit

// Create a RDCircleProgressView
let circleProgressView = RDCircleProgressView(frame: CGRect(x: 50, y: 50, width: 100, height: 100))

// Customize properties
circleProgressView.image = UIImage(named: "profile")
circleProgressView.seenProgressColor = .blue
circleProgressView.unseenProgressColor = .lightGray
circleProgressView.lineWidth = 5.0
circleProgressView.total = 10

// Set progress with animation
circleProgressView.setProgress(progress: 6, animated: true)

// Add to your view hierarchy
view.addSubview(circleProgressView)
```

### **Using Interface Builder**

1. Add a `UIView` to your **Storyboard** or **XIB**.
2. In the **Identity Inspector**, set the class to `RDCircleProgressView`.
3. Customize properties directly in the **Attributes Inspector**, such as:
   - `image`
   - `seenProgressColor`
   - `unseenProgressColor`
   - `lineWidth`
   - `imageInset`
   - `clockwise`

---

## **Customization Options**

| **Property**            | **Description**                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------|
| `image`                 | The central image displayed within the circular progress view.                                       |
| `seenProgressColor`     | The color of the completed portion of the circular progress.                                         |
| `unseenProgressColor`   | The color of the remaining (uncompleted) portion of the progress circle.                             |
| `lineWidth`             | Specifies the thickness of the progress stroke.                                                     |
| `total`                 | Sets the total number of progress segments (e.g., 100 for percentages or a specific count).          |
| `progress`              | Updates the current progress value. Use the method `setProgress(progress:animated:)` to animate it. |
| `clockwise`             | A Boolean indicating whether progress is drawn clockwise (`true`) or counterclockwise (`false`).    |

---

## **Examples**

Try setting up a basic `RDCircleProgressView` in a new project or directly in Interface Builder. Experiment with different configurations to see its capabilities in action.

---

## **Contributing**

We welcome contributions to enhance this library. If you encounter a bug, have a feature request, or want to submit a pull request, please check out our contribution guidelines.

---

## **License**

RDCircleProgressKit is available under the MIT License. See the [LICENSE](LICENSE) file for more details.
