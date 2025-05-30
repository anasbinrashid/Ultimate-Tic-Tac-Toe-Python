# Ultimate Tic-Tac-Toe AI Championship

A sophisticated implementation of Ultimate Tic-Tac-Toe featuring multiple AI difficulty levels powered by Constraint Satisfaction Problem (CSP) algorithms, Minimax with Alpha-Beta pruning, and advanced heuristics.

## Game Overview

Ultimate Tic-Tac-Toe is a strategic variant of the classic game played on a 3×3 grid of 3×3 boards. Your move determines which board your opponent must play in next, creating deep strategic gameplay that requires both tactical and strategic thinking.

### Key Features

- **Advanced AI System**: Three difficulty levels with different algorithms
  - **Easy**: Random move selection
  - **Medium**: Strategic play with win/block detection
  - **Hard**: CSP-based AI with Minimax, Alpha-Beta pruning, and constraint propagation
- **Multiple Game Modes**: Human vs Human, Human vs AI, AI vs AI
- **Modern UI**: Dark theme with visual feedback and board highlighting
- **Game Logging**: Comprehensive move tracking and game state logging
- **Real-time Gameplay**: Smooth animations and responsive controls

## AI Architecture

### CSP (Constraint Satisfaction Problem) Implementation

The advanced AI uses CSP techniques to make optimal moves:

- **Variables**: Empty cells in active small boards
- **Domains**: Valid player symbols ('X' or 'O')
- **Constraints**: Game rules (valid moves, board states, win conditions)

### Advanced Algorithms

1. **Minimax with Alpha-Beta Pruning**
   - Depth-limited search (3 levels for optimal performance)
   - Alpha-beta pruning for efficiency
   - Position evaluation heuristics

2. **Constraint Propagation**
   - **Forward Checking**: Eliminates inconsistent future moves
   - **Arc Consistency (AC-3)**: Maintains constraint consistency
   - **MRV Heuristic**: Minimum Remaining Values for variable ordering

3. **Strategic Heuristics**
   - Center position preference
   - Corner strategy implementation
   - Board constraint analysis
   - Win/block pattern recognition

## Installation & Setup

### Prerequisites

- Python 3.7 or higher
- tkinter (usually included with Python)

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/ultimate-tictactoe-ai.git
cd ultimate-tictactoe-ai

# Run the game
python ultimate_tictactoe.py
```

### Alternative Installation

```bash
# If you prefer to download directly
wget https://raw.githubusercontent.com/yourusername/ultimate-tictactoe-ai/main/ultimate_tictactoe.py
python ultimate_tictactoe.py
```

## How to Play

### Game Rules

1. **Board Structure**: 3×3 grid of small tic-tac-toe boards
2. **Move Constraints**: Your move determines which small board your opponent plays in next
3. **Winning**: Win three small boards in a row (horizontally, vertically, or diagonally)
4. **Free Play**: If sent to a completed board, play anywhere

### Controls

- **Click** any valid cell to make your move
- **NEW GAME** button to restart
- **Mode Dropdown** to switch between game modes
- **Visual Feedback**: Active boards are highlighted in red

### Game Modes

- **Human vs Human**: Classic two-player mode
- **Human vs AI**: Challenge the computer
- **AI vs AI**: Watch AI strategies compete

## Technical Implementation

### Core Classes

#### `UltimateTicTacToe`
Main game class handling:
- GUI rendering and event handling
- Game state management
- Move validation and execution
- AI move coordination

#### `UltimateTicTacToeCSP`
CSP implementation providing:
- Constraint satisfaction algorithms
- Variable and domain management
- Arc consistency checking
- Backtracking search

### Key Algorithms

```python
# CSP-based move selection
def ai_csp_move(self):
    """Advanced AI using CSP approach with minimax"""
    # Minimax with alpha-beta pruning
    # Forward checking and arc consistency
    # Move ordering with MRV heuristic
```

### Data Structures

- **4D Board Array**: `board[big_row][big_col][small_row][small_col]`
- **Small Board Status**: Tracks won/drawn small boards
- **Move Constraints**: Next valid board tracking
- **Game State**: Current player, game status, winner

## Performance Optimization

### Alpha-Beta Pruning
- Reduces search space by ~50%
- Move ordering for maximum pruning efficiency
- Depth limitation for real-time play

### Constraint Propagation
- Forward checking eliminates invalid moves early
- Arc consistency maintains global consistency
- MRV heuristic improves search efficiency

### Memory Management
- Deep copy for state preservation
- Efficient board representation
- Minimal memory allocation during search

## UI/UX Features

### Visual Design
- **Dark Theme**: Modern, easy-on-eyes color scheme
- **Color Coding**: 
  - Red (#ff5722) for X moves
  - Teal (#4ecca3) for O moves
  - Pink (#e94560) for active board highlighting
- **Responsive Layout**: Adapts to different screen sizes

### User Feedback
- **Real-time Status**: Current player and board information
- **Move Highlighting**: Visual indication of valid moves
- **Win Animations**: Board color changes for won states
- **Game Logging**: Timestamped move history

## Game Statistics & Logging

The game automatically logs all moves and events to `ultimate_tictactoe_log.txt`:

```
[2024-05-31 14:30:15] New game started
[2024-05-31 14:30:15] Mode: Human vs AI
[2024-05-31 14:30:20] Player X moved at big board (1,1), small position (1,1)
[2024-05-31 14:30:22] AI (O) selected move: big board (1,1), small position (0,0)
```

## Testing & Validation

### AI Performance Testing
- Move quality assessment
- Constraint satisfaction verification
- Performance benchmarking
- Edge case handling

### Game Logic Validation
- Win condition checking
- Move validation testing
- State consistency verification
- UI synchronization testing

## Contributing

Contributions are welcome! Here's how you can help:

### Development Setup
```bash
git clone https://github.com/yourusername/ultimate-tictactoe-ai.git
cd ultimate-tictactoe-ai
# Make your changes
# Test thoroughly
# Submit pull request
```

### Contribution Guidelines
- Follow PEP 8 style guidelines
- Add comprehensive comments
- Include test cases for new features
- Update documentation as needed

### Areas for Contribution
- AI algorithm improvements
- UI/UX enhancements
- Performance optimizations
- Bug fixes and testing
- Documentation improvements

## Acknowledgments

- **CSP Algorithms**: Based on Russell & Norvig's "Artificial Intelligence: A Modern Approach"
- **Game Theory**: Minimax and Alpha-Beta pruning implementations
- **UI Design**: Modern dark theme inspired by contemporary game interfaces
- **Python Community**: For excellent libraries and documentation
