# Jeu de Taquin

A console-based Taquin game implemented in C#.

## Project Overview

This game was created as a team project during my second semester in software development.

The objective of the Taquin game is to rearrange numbered tiles that have been shuffled. The grid's dimensions can vary, for example, a 4 x 4 grid:

(Wikipedia - Free Encyclopedia, 2022)

The player must move a numbered tile to the empty space to solve the grid by arranging the numbers in ascending order. The numbers should be displayed in numerical order: 1, 2, 3, ... The goal is to solve the grid with the fewest moves.

### Project Structure

- **Version Control (DevOps – Azure Repos GIT):** Form a team of two people and inform your instructor via MIO. In LÉA, an Excel file will contain the DevOps – GIT link for your team, which you should use for GIT transactions.

### Instructions

1. During the project design, each team member must make a minimum of 5 modifications and push them to the central repository. Provide meaningful comments for each pushed modification.
   - `Program.cs` should contain only code related to information requests and displays, fueled by calls to members of the `JeuTaquin` class.
   - `JeuTaquin` class should encapsulate all the logic of the Taquin game.
      - No information requests.
      - No displays.

2. Create the solution `JeuTaquin` and the project `JeuTaquinConsole` of type Console (.NET Core) and structure it according to MVVM. Make an initial repository deposit. Ensure that each member can retrieve this project and operate with GIT.

## Programming the `JeuTaquin` Class and Console (.NET Core)

Create a class named `JeuTaquin` to encapsulate the logic associated with the Taquin game. Program the properties and methods as described below:

### Properties

- **Deplacements:** Keeps track of the number of moves made.
- **Grille:** Provides access to the content of the internal grid (managed internally). Used to populate the display.
- **Record:** Memorizes the smallest number of moves made to solve a grid.

### Methods

- **DeplacerVers(Direction direction):** Moves the number towards the empty space if allowed. This method will be called in `Program.cs` when the user presses an arrow key.
- **DeterminerGrilleResolue():** Validates if all the numbers in the grid are in the correct position. Indicates if the player has won or not.
- **InitialiserGrille():** Prepares the grid by shuffling the numbers in a solvable manner. This method should be called just before starting a game or when the player wants to restart.
- **Permuter(int position1, int position2):** Private method to exchange the value in one position with another.
- **Resoudre():** Places the numbers in the correct order on the grid. Useful for validating the victory message and will be used in TP2.

### Implementation Guidelines

- Focus the game logic in the `JeuTaquin` class.
- Declare a `JeuTaquin` object in `Program.cs` and use it (Call its members).
- Use arrow keys to move a number near the empty space (highlighted in red). Hints: Use `ReadKey()`, the `Key` property, and the `ConsoleKey` enumeration (refer to documentation).
- Implement operations: Quit, Restart, and Solve.
