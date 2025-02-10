# Quick Tic-Tac-Toe Game
# A simple two-player Tic-Tac-Toe in Python.

# Initialize board
board = [" "] * 9
players = ["X", "O"]

# Function to display the board
def display():
    print("\n" + "\n---|---|---\n".join(
        f" {board[i]} | {board[i+1]} | {board[i+2]} " for i in range(0, 9, 3)
    ) + "\n")

# Function to check for a winner
def winner():
    for a, b, c in [(0,1,2), (3,4,5), (6,7,8), (0,3,6), (1,4,7), (2,5,8), (0,4,8), (2,4,6)]:
        if board[a] == board[b] == board[c] != " ":
            return board[a]
    return None

# Game loop
print("Welcome to Tic-Tac-Toe!")
for turn in range(9):
    display()
    while True:
        try:
            move = int(input(f"Player {players[turn % 2]}, enter (1-9): ")) - 1
            if board[move] == " ":
                board[move] = players[turn % 2]
                break
        except (ValueError, IndexError):
            pass
        print("Invalid move, try again.")

    if winner():
        display()
        print(f"Player {winner()} wins!")
        break

    display()
    print("It's a draw!")
