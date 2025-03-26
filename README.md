# Attack On Titan: Utopia
<a href="#contribution-guidelines"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome"></a>
<a href="#license"><img alt="Static Badge" src="https://img.shields.io/badge/License-Custom%20License%20v1.2-blue">
## Project Description
**Attack On Titan: Utopia** is a one-player, endless tower defense game inspired by the hit anime *Attack on Titan*. The game is set in the Utopia District of Wall Rose, where players must defend against waves of titans using a variety of Anti-Titan weapons. The objective is to prevent the titans from breaching the walls of Utopia for as long as possible.

## Table of Contents
- [Preview](#preview)
  - [Screenshots](#screenshots)
  - [Gameplay Video](#gameplay-video)
- [Installation](#installation)
  - [IntelliJ IDEA](#intellij-idea)
  - [Eclipse](#eclipse)
- [Dependencies](#dependencies)
- [Game Elements](#game-elements)
  - [Phases](#phases)
  - [Titans](#titans)
  - [Weapons](#weapons)
  - [Game Rules](#game-rules)
  - [Turn Actions](#turn-actions)
- [Credits](#credits)
- [License](#license)
- [Contribution Guidelines](#contribution-guidelines)
- [Commercial Use](#commercial-use)
## Preview

### Screenshots

![Start Page](https://github.com/user-attachments/assets/7a3a9122-ab7b-4b66-b678-c23add98bf9c)
![Video Scene](https://github.com/user-attachments/assets/9b627df8-85e3-4f4f-ab55-ac9940024452)
![Game Settings](https://github.com/user-attachments/assets/d6b3176f-9bc9-4664-961f-01ff81a9895e)
![Game Instructions](https://github.com/user-attachments/assets/43001df5-359c-4863-8112-17597fbf32a3)
![Easy Mode](https://github.com/user-attachments/assets/ec55875f-a8fd-4fd4-9685-9f854707fa7f)
![Hard Mode](https://github.com/user-attachments/assets/28b2ec58-0e4b-40a4-9f1a-d7dbf183f9dd)



### Gameplay Video

*Embed a gameplay video or provide a link to a video showcasing the game.* [To Be Added]

## Installation

### IntelliJ IDEA
To get started with **Attack On Titan: Utopia** in IntelliJ IDEA, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yehiarasheed/Attack-On-Titan-Utopia.git
    cd Attack-On-Titan-Utopia
    ```

2. **Open the project in IntelliJ IDEA**:
    - Go to `File` > `Open...` and select the project directory.
    - Ensure the correct JDK is set up for the project (JDK 11 or higher).

3. **Set up JavaFX**:
    - Download the JavaFX SDK from the [Gluon JavaFX download page](https://gluonhq.com/products/javafx/).
    - Extract the JavaFX SDK to a directory on your computer.
    - Go to `File` > `Project Structure...` > `Libraries` and add the JavaFX `lib` directory.
    - Go to `Run` > `Edit Configurations...` and add VM options to include the JavaFX libraries:

       ```plaintext
      --module-path /path_to_javafx_lib --add-modules javafx.controls,javafx.fxml,javafx.media
      ```

4. **Build and run the project**:
    - Build the project by going to `Build` > `Build Project`.
    - Run the project by selecting the main class and clicking the run button.

### Eclipse
To get started with **Attack On Titan: Utopia** in Eclipse, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yehiarasheed/Attack-On-Titan-Utopia.git
    cd Attack-On-Titan-Utopia
    ```

2. **Open the project in Eclipse**:
    - Go to `File` > `Import...` > `Existing Projects into Workspace`.
    - Select the cloned repository directory.

3. **Set up JavaFX**:
    - Download the JavaFX SDK from the [Gluon JavaFX download page](https://gluonhq.com/products/javafx/).
    - Extract the JavaFX SDK to a directory on your computer.
    - Go to `Project` > `Properties` > `Java Build Path` > `Libraries` > `Modulepath` > `Add External JARs...` and add all the JAR files from the JavaFX `lib` directory.
    - Go to `Run` > `Run Configurations...` and add VM options to include the JavaFX libraries:

      ```plaintext
      --module-path /path_to_javafx_lib --add-modules javafx.controls,javafx.fxml,javafx.media
      ```

4. **Build and run the project**:
    - Right-click on the project and select `Build Project`.
    - Run the project by selecting the main class and clicking the run button.

## Dependencies
This software depends on the following applications:
- **JavaFX:** Required for the user interface. You can download the JavaFX SDK from the [Gluon webpage](https://gluonhq.com/products/javafx/).
- **JDK 11 or higher:** Java Development Kit (JDK) is a software development environment needed to develop Java applications and applets.

For more information on setting up JavaFX, refer to the [Bro Code JavaFX Playlist](https://www.youtube.com/watch?v=_7OM-cMYWbQ&list=PLZPZq0r_RZOM-8vJA3NQFZB7JroDcMwev).

## Game Elements
- **Titans**: Enemies with various stats like HP, Damage, Speed, and special traits.
- **Weapons**: Defensive tools with different attack behaviors and costs.
- **Wall Parts**: Defensive structures with HP that need to be protected.

### Phases

The game progresses through different phases based on the number of turns elapsed:

- **Early Phase**: Minimal titan spawns, allowing players to build up defenses.
- **Intense Phase**: Increased titan spawns, including tougher titan types, testing player strategies.
- **Grumbling Phase**: The most difficult phase with frequent spawns of the largest titans, requiring players to use all their resources and tactics to survive.

**Each Phase a total of seven titans spawn, spawning one titan in each turn except for the last part of the _Grumbling Phase_**

| Phase           | Description                                                     | Titan Types              | Difficulty Level |
|-----------------|-----------------------------------------------------------------|--------------------------|------------------|
| Early Phase     | Minimal titan spawns, allowing players to build up defenses.    | Pure Titan, Abnormal Titan | Low              |
| Intense Phase   | Increased titan spawns, including tougher titan types.          | Pure Titan, Abnormal Titan, Armored Titan | Medium           |
| Grumbling Phase | Most difficult phase with frequent spawns of the largest titans.| Pure Titan, Abnormal Titan, Armored Titan, Colossal Titan | High              |

### Titans

#### Types of Titans

| Type          | HP   | Damage | Height | Speed | Resources Value | Danger Level | Special Trait               |
|---------------|------|--------|--------|-------|-----------------|--------------|-----------------------------|
| Pure Titan    | 100  | 15     | 15     | 10    | 10              | 1            | -                           |
| Abnormal Titan| 100  | 20     | 10     | 15    | 15              | 2            | Attacks twice per turn      |
| Armored Titan | 200  | 85     | 15     | 10    | 30              | 3            | Takes only 25% damage       |
| Colossal Titan| 1000 | 100    | 60     | 5     | 60              | 4            | Increases speed each move   |

### Weapons

#### Types of Weapons

| Weapon Type       | Price | Damage | Attack Action                           |
|-------------------|-------|--------|-----------------------------------------|
| Piercing Cannon   | 25    | 10     | Attacks closest 5 titans to the wall     |
| Sniper Cannon     | 25    | 35     | Attacks the first closest titan to wall  |
| Volley Spread Cannon | 100 | 5      | Attacks all titans between min and max range |
| Wall Trap         | 75    | 100    | Attacks a titan that reached the walls   |

### Game Rules

- **Winning and Losing Conditions**: The game has no winning condition; players aim to survive as long as possible. Losing occurs when all wall parts are destroyed.
- **Titan Movement**: Titans move closer to the wall each turn based on their speed.
- **Attack Actions**: Titans and weapons perform attack actions each turn, affecting wall parts and titans respectively.
- **Defeated Targets**: Defeated titans add resources and score to the player. Destroyed wall parts render lanes inactive.

### Turn Actions

Each turn, players can choose to deploy weapons or pass. Turn sequence involves titan movement, weapon attacks, new titan spawns, and phase updates.

## Credits
- **Developers**: Jomana Mahmoud, Nada Yasser & Yehia Rasheed.
- **Inspired by**: *Attack on Titan* anime series

All media used in this project, including images and videos, are credited to their respective creators and used under fair use for educational and demonstration purposes. If you plan to use this project for commercial purposes, you must ensure you have obtained the necessary licenses or permissions for any copyrighted media.

## License

This project is licensed under the **Attack On Titan: Utopia License - Version 1.2**. See the [LICENSE](./LICENSE.md) file for details.

### License Summary

- **License Grant**: You are granted a non-exclusive, worldwide, royalty-free, perpetual license to use, modify, distribute, and contribute to the project.
- **Contributions**: Contributions must be submitted via GitHub pull requests and are subject to review and approval.
- **Commercial Use**: Requires separate agreement with the project owners. Notification and licensing for commercial use are required.
- **Attribution**: Proper credit must be given to the project and its media sources.
- **Disclaimer**: The project is provided "as is" without warranties.
- **Termination**: License may be terminated for non-compliance.

For full license terms, please refer to the [LICENSE](./LICENSE.md) file.

## Contribution Guidelines

We’re excited that you’re interested in contributing to this project! Whether it's fixing bugs, adding features, or improving documentation, your contributions are welcome and appreciated.

For more detailed information on how to contribute, please check out our [CONTRIBUTING.md](./CONTRIBUTING.md) file.

### How to Contribute

- **Submit a Pull Request**: If you’ve made changes that you think will benefit the project, please submit a pull request on GitHub.
- **Review Process**: All contributions will be reviewed by the project owners. We’ll provide feedback, and once everything looks good, your changes will be merged into the project.
- **Discretion**: Contributions will be incorporated into the project at the discretion of the project owners, but don’t worry—your work is valued, and we’ll do our best to include it if it fits with the project’s goals.

Thank you for helping make this project better!
## Commercial Use

If you intend to use this project for commercial purposes, please follow these steps:

1. **Contact**: Reach out to the project owners at [yehiarasheed@gmail.com](mailto:yehiarasheed@gmail.com) to request permission for commercial use. Notification and licensing from original copyright holders for commercial use are required.
2. **Agreement**: A separate agreement must be made with the project owners regarding commercial use. This may include terms for revenue sharing or other considerations.

---
