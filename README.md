# BetterJFrame Library

## Overview

**BetterJFrame** is a Java library designed to enhance user experience and simplify the process of building graphical user interfaces (GUIs). It provides a set of customizable components and utilities that make UI development more efficient and visually appealing.

## Table of Contents

1. [Features](#features)
2. [Getting Started](#getting-started)
3. [Installation](#installation)
4. [Usage](#usage)
   - [Core Components](#core-components)
   - [Buttons](#buttons)
   - [Labels](#labels)
   - [Text Fields](#text-fields)
   - [Panels](#panels)
   - [Utilities](#utilities)
5. [Customization](#customization)
6. [Examples](#examples)
7. [Contributing](#contributing)
8. [License](#license)

## Features

- **Customizable Components:** Provides a variety of UI components such as buttons, labels, text fields, and panels that can be easily customized.
- **Animations:** Built-in support for animations, enhancing the user interface with smooth transitions.
- **Layout Utilities:** Simplifies layout management with various layout utilities.
- **Notifications:** Toast notifications and progress indicators for better user feedback.
- **Validation:** Input validation utilities to ensure correct data entry.
- **Theme Support:** Easily customizable themes for a consistent look and feel.

## Getting Started

To get started with the BetterJFrame library, ensure you have Java Development Kit (JDK) installed. This library is compatible with JDK 8 and above.

## Installation

You can include the BetterJFrame library in your project by downloading the latest release from the [GitHub repository](link-to-repo) or by adding it as a dependency in your build tool (e.g., Maven, Gradle).

### Maven

```xml
<dependency>
    <groupId>me.kammoun</groupId>
    <artifactId>BetterJFrame</artifactId>
    <version>1.0.0</version>
</dependency>
```

### Gradle

```groovy
implementation 'me.kammoun:BetterJFrame:1.0.0'
```

## Usage

### Core Components

#### BJFrame

The main application window. It serves as the foundation for your GUI applications.

```java
import me.kammoun.Core.BJFrame;

public class MyApplication {
    public static void main(String[] args) {
        BJFrame frame = new BJFrame("My Application");
        frame.setSize(800, 600);
        frame.setVisible(true);
    }
}
```

### Buttons

#### BJRoundButton

A button with rounded corners.

```java
import me.kammoun.Buttons.BJRoundButton;

BJRoundButton roundButton = new BJRoundButton("Click Me");
roundButton.addActionListener(e -> {
    System.out.println("Button Clicked!");
});
```

### Labels

#### BJLabel

A customizable label that can be made clickable.

```java
import me.kammoun.Text.BJLabel;

BJLabel label = new BJLabel("Hello, World!");
label.setClickable(true);
label.setOnClick(e -> {
    System.out.println("Label Clicked!");
});
```

### Text Fields

#### BJTextField

A customizable text field with various enhancements.

```java
import me.kammoun.TextField.BJTextField;

BJTextField textField = new BJTextField();
textField.setPlaceholder("Enter your name");
```

### Panels

#### BJGradientPanel

A panel that supports gradient backgrounds.

```java
import me.kammoun.Panels.BJGradientPanel;

BJGradientPanel gradientPanel = new BJGradientPanel();
gradientPanel.setGradientColors(Color.BLUE, Color.GREEN);
```

### Utilities

#### BJColorUtils

Utilities for color manipulation.

```java
import me.kammoun.utils.BJColorUtils;

Color blendedColor = BJColorUtils.blend(Color.RED, Color.BLUE, 0.5);
```

## Customization

The BetterJFrame library allows you to customize components easily. You can modify properties such as colors, fonts, sizes, and more through dedicated setter methods. 

### Themes

You can define custom themes using the `BJThemes` class to ensure consistency across your application.

## Examples

Here's a simple example of a BetterJFrame application:

```java
import me.kammoun.Core.BJFrame;
import me.kammoun.Buttons.BJRoundButton;
import me.kammoun.Text.BJLabel;

public class ExampleApp {
    public static void main(String[] args) {
        BJFrame frame = new BJFrame("Example Application");
        BJLabel label = new BJLabel("Welcome to BetterJFrame!");
        BJRoundButton button = new BJRoundButton("Press Me");

        button.addActionListener(e -> {
            label.setText("Button Pressed!");
        });

        frame.add(label);
        frame.add(button);
        frame.setLayout(new FlowLayout());
        frame.setSize(400, 300);
        frame.setVisible(true);
    }
}
```

## Contributing

Contributions are welcome! If you'd like to contribute to the BetterJFrame library, please fork the repository and submit a pull request. For larger changes, consider opening an issue to discuss your ideas.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
