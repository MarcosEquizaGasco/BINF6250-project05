# Introduction
Description of the project

# Pseudocode
Put pseudocode in this box:

```
Smith-Waterman Algorithm:

Call scoring function to create matrix and get position of best score

    Initialize matrix with zeroes (use np.zeros(i,j)) --> i is rows (len(seq1)), j is columns (len(seq2))
    
    Iterate through each position (walk through each row) and call scoring function (exclude first row and columm)

    Update matrices with score and traceback move for that position

Find max value in matrix --> find argmax and unravel to get coordinates

Call traceback function with recorded moves to get aligned seqs & score

Print aligned sequences and the alignment score

Calculate Score:
Check if seqs match or mismatch at position (i, j) --> string evaluation

Create dictionary {'0-END': 0, '1-DIAG': 0, '2-UP': 0, '3-LEFT': 0} to track moves and scores

Calculate diagonal score

    Take score at matrix(i-1, j-1)

    If we have a match --> add match value to score

    Else --> add mismatch value to score

Calculate up score

    Take score at matrix(i-1, j) and add gap value

Calculate left score

    Take score at matrix(i, j-1) and add gap value

Take max value as score

Return score and direction of that score (we can use the dictionary)

Traceback:
Start at max position

Identify starting bases for seq1 (maximum_position[0]) and seq2 (maximum_position[2])

Access move in traceback_matrix using maximum_position

Iterate through each of the moves until we end at a "END" move (while loop)

    current_position (row, column)
    current_move (string)

    If curent move is DIAG

        Extend aligned_seq1 with the corresponding base from seq1 (seq1[row])
        Extend aligned_seq2 with the corresponding base from seq2 (seq2[column])
        Update current_position to matrix[row-1, column-1]

    If current move is UP

        Extend aligned_seq1 with the corresponding base from seq1 (seq1[row])
        Extend aligned_seq2 with - (vertical gap)
        Update current_position to matrix[row-1, column]

    If current move is LEFT

        Extend aligned_seq1 with - (horizontal gap)
        Extend aligned_seq2 with the corresponding base from seq2 (seq2[column])
        Update current_position to matrix[row, column-1]

Reverse aligned_seqs (so they are in order)

Return the aligned sequences 
```

# Successes
Description of the team's learning points

# Struggles
Description of the stumbling blocks the team experienced

# Personal Reflections
## Group Leader
Group leader's reflection on the project

## Other member
Other members' reflections on the project

# Generative AI Appendix
As per the syllabus
