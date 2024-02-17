# Cybersecurity-Project

Overview: Small program that encrypts alphabetic letters using the Hill cipher with a matrix any size 2x2 to 9x9

Compiles and runs on terminal command line. First parameter is the name of the encryption key file, and the second parameter is the name of the file to be encrypted. Opens two files, echos the processed input to the screena and makes the necessary calculations, and then outputs the ciphertext to the console screen. 

Encryption key file formats: The encryption key file contains a single positive integer, n where (1<n<10), on the first line indicating hte number of rows/columns in the encryption matrix. The following n lines will contain n integers, in each row, in order, of the encryption matrix, separated by spaces. 

Encryption Plaintext file formats: The file to be encrypted can be any valid text file with no more than 9,991 letters in it. (Thus, it’s safe to store all characters in the file in a character array of size 10,000, including any padding characters.) Please note that the input text file will also generally have punctuation, numbers, special characters, and whitespace in it, which should be ignored. The programs also convers uppercase letters to lowercase in the input file, correspondingly lowercase letters do not need to be converted. Thus, the program will treat A and a the same. 

Output format: The program must output the following to the console (terminal) screen, also known as stdout:
    1. Echothenumbersfromtheinputkeyfile.
    2. Echothelowercasealphabetictextderivedfromtheinputplaintextfile.
    3. Ciphertext output produced from encrypting the input key file against the input array specified in the key file.
    
  The output portion of the input plaintext file should consist of only lowercase letters in rows of exactly 80 letters per row, except for the last row, which may possibly have fewer. These characters should correspond to the ciphertext produced by encrypting using the numbers collected from the input key file and applied as a Hill cipher, via matrix multiplication. 

  Matrix multiplication review: In mathematics, particularly in linear algebra, matrix multiplication is a binary operation that produces a matrix from two matrices. For matrix multiplication, the number of columns in the first matrix must be equal to the number of rows in the second matrix. The resulting matrix, known as the matrix product, has the number of rows of the first and the number of columns of the second matrix. The product of matrices A and B is denoted as AB. In the pseudocode below, the product AB is C
Remember that in the Hill Cipher the key matrix has the same number of columns as rows, and is also known a square matrix.
  Algorithm for matrix multipication:
    if A.columns DO NOT EQUAL B.rows then
      errors dimensions
    else
      let C be a new A.rows X B.columns matrixs
      for i=1 -> B.columns do
        cij = 0 
        for k = 1 -> A.columns do
          cij = cij + aik x bjk
    RETURN C
