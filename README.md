# 🔄 Push Swap

A 42 project sorting a stack of integers using a limited set of operations, with the fewest moves possible.

---

## Introduction

Push Swap is a sorting algorithm project. Given a stack of integers **stack A**, the goal is to sort them in ascending order using a second stack **stack B** and a restricted set of operations.

The challenge is to find the most **efficient sequence of operations** to sort the stack.

### Key Concepts

- **Stack data structure** — LIFO (Last In First Out) implemented with a linked list
- **Greedy algorithm** — at each step, pushing the element with the lowest move cost
- **Target system** — each element in stack A targets its optimal position in stack B
- **Push cost** — calculating the minimum number of moves to bring an element to the top
- **Combined rotations** — using `rr` and `rrr` to rotate both stacks simultaneously and save moves

---

## Usage

### Compilation

```bash
make        # Compile the project
make clean  # Remove object files
make fclean # Remove object files and binary
make re     # Full recompilation
```

### Running

```bash
./push_swap 3 1 2 5 4
```

Or with a string of numbers :

```bash
./push_swap "3 1 2 5 4"
```

### Generate random numbers

To test with a large random set, use this command to generate N random numbers :

```bash
# Generate 100 random numbers and run push_swap
./push_swap $(shuf -i 1-1000 -n 100 | tr '\n' ' ')
```
---

## Log Format

Each line printed to stdout represents **one operation performed** to sort the stack.

```
pb
pb
ra
rr
pa
sa
pa
```

> The total number of lines = the total number of operations used.  

---

## Available Operations

| Operation | Description |
|---|---|
| `sa` | Swap the first 2 elements of stack A |
| `sb` | Swap the first 2 elements of stack B |
| `ss` | `sa` and `sb` simultaneously |
| `pa` | Push the top of stack B to stack A |
| `pb` | Push the top of stack A to stack B |
| `ra` | Rotate stack A upward (first element becomes last) |
| `rb` | Rotate stack B upward |
| `rr` | `ra` and `rb` simultaneously |
| `rra` | Reverse rotate stack A (last element becomes first) |
| `rrb` | Reverse rotate stack B |
| `rrr` | `rra` and `rrb` simultaneously |

---

## Author

Made by [Arthur-PRZ](https://github.com/Arthur-PRZ)
