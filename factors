#!/usr/bin/python3
import sys
import math


"""
This script is used to factorize a number into two prime numbers.
The script takes a file as input.
where each line contains a number to be factorized.
The script outputs the two prime factors of each number in the file.
"""


def factorize_number(num):
    """
        Factorize a number into two prime numbers.
        param num: number to be factorized
        p: first prime factor
        q: second prime factor
        sq: square root of the number
        i: iterator
        return: two prime factors of the number
    """

    if num % 2 == 0:
        p = num // 2
        q = 2
        print(f"{num}={p}*{q}")
    else:
        sq = int(math.sqrt(num) + 1)
        for i in range(3, sq, 2):
            if num % i == 0:
                p = num // i
                q = i
                print(f"{num}={p}*{q}")
                return

            if num % (sq + 1) == 0:
                p = num // (sq + 1)
                q = sq + 1
                print(f"{num}={p}*{q}")
                return

            if num % (sq - 1) == 0:
                p = num // (sq - 1)
                q = sq - 1
                print(f"{num}={p}*{q}")
                return
    return p, q


def factorize_file(filename):
    """
    Factorize numbers in a file.
    param filename: file containing numbers to be factorized
    """
    with open(filename, encoding="utf-8") as file:
        for line in file.readlines():
            number = int(line.strip())
            factorize_number(number)


if __name__ == '__main__':
    """
    Main function.
    param filename: file containing numbers to be factorized
    argv[1]: filename
    """
    if len(sys.argv) != 2:
        print("Usage: python3 factors.py <filename>")
        sys.exit(1)
    filename = sys.argv[1]
    factorize_file(filename)
