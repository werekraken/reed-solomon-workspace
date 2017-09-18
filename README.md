# Reed-Solomon Workspace

Workspace to play with Reed-Solomon.

This code contains a partial port of the [Backblaze/JavaReedSolomon](https://github.com/Backblaze/JavaReedSolomon) library.

For an introduction on erasure coding, see the post on the [Backblaze blog](https://www.backblaze.com/blog/reed-solomon/).

## simple-gf2-times-demo.rb Output
```
# Original data.
    # 583ef0ac
    [[65, 66, 67, 68],
     [69, 70, 71, 72],
     [73, 74, 75, 76],
     [77, 78, 79, 80]]

# Magic matrix to create 2 parity blocks.
    # 7e2a5356
    [[1, 0, 0, 0],
     [0, 1, 0, 0],
     [0, 0, 1, 0],
     [0, 0, 0, 1],
     [27, 28, 18, 20],
     [28, 27, 20, 18]]

# Magic matrix to repair up to 2 missing blocks.
    # da17d55d
    [[1, 0, 0, 0],
     [0, 1, 0, 0],
     [0, 0, 1, 0],
     [0, 0, 0, 1],
     [141, 246, 123, 1],
     [246, 141, 1, 123]]

# Original data with 2 parity blocks appended.
    # 81870e91
    [[65, 66, 67, 68],
     [69, 70, 71, 72],
     [73, 74, 75, 76],
     [77, 78, 79, 80],
     [81, 82, 83, 73],
     [85, 86, 87, 37]]

# Damaged data with 2 parity blocks appended and 2 data blocks missing.
    # 88afae54
    [[65, 66, 67, 68],
     [69, 70, 71, 72],
     [81, 82, 83, 73],
     [85, 86, 87, 37]]

# Magic matrix to repair damage (corresponding rows to the damaged blocks have been removed).
    # e550822e
    [[1, 0, 0, 0],
     [0, 1, 0, 0],
     [141, 246, 123, 1],
     [246, 141, 1, 123]]

# Repaired data.
    # 583ef0ac
    [[65, 66, 67, 68],
     [69, 70, 71, 72],
     [73, 74, 75, 76],
     [77, 78, 79, 80]]

Original data marshaled matrix crc32: 583ef0ac
Repaired data marshaled matrix crc32: 583ef0ac
```
