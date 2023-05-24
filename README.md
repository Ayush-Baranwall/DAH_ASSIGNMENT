# Implementing MapReduce in Python

## MapReduce Algorithm Implementation

This repository contains an implementation of the MapReduce algorithm using the `multiprocessing` module in Python. The MapReduce algorithm is a programming model for processing and analyzing large datasets in a distributed and parallel manner.

## Usage

To use this implementation, follow the instructions below:

1. Clone the repository to your local machine:

   ```
   git clone https://github.com/Ayush-Baranwall/Implementing-MapReduce-in-Python.git
   ```

2. Navigate to the repository directory:

   ```
   cd Ayush-Baranwall
   ```

3. Ensure that you have Python installed on your machine. This code is compatible with Python 3.

4. Install the required dependencies using pip:

   ```
   pip install -r requirements.txt
   ```

5. Create an input file named `input.txt` and populate it with the text data you want to process.

6. Open the `map_reduce.py` file in a text editor and make the following modifications:

   - Adjust the `map_worker` function according to your specific data processing requirements. This function takes a chunk of text as input and performs the mapping operation on it.

   - Modify the `reduce_worker` function as needed. This function receives the output from the shuffle step and performs the reducing operation.

   - Customize the `main` function if desired, keeping in mind that it currently invokes the `map_worker` function on the entire input text and prints the result.

7. Save the changes to `map_reduce.py` and execute the script:

   ```
   python map_reduce.py
   ```

   The script will read the input text from the `input.txt` file, perform the MapReduce operations based on the defined functions, and display the output.

## Algorithm Explanation

The MapReduce algorithm implemented in this code consists of the following steps:

1. **Read the Input File and Split into Chunks**: The input data is read from the `input.txt` file and divided into chunks based on the number of specified map workers.

2. **Map Step**: The map worker function is applied to each chunk of data in parallel using multiprocessing. The map worker counts the occurrences of each word in the chunk and returns a list of word-count pairs.

3. **Shuffle Step**: The map results are combined into a single list of word-count tuples. The shuffle worker function then groups the tuples by word, creating a dictionary where each word is associated with a list of its respective counts.

4. **Reduce Step**: The shuffle results are combined into a single list of word-count tuples. The reduce worker function is applied to each tuple in parallel using multiprocessing. The reduce worker sums the counts for each word and returns a list of word-total count pairs.

5. **Final Results**: The final word-total count pairs are obtained by combining the results from the reduce step. These results can be further processed or analyzed as required.

## Contributing

If you would like to contribute to this project, you can follow these steps:

1. Fork the repository on GitHub.

2. Clone your forked repository to your local machine.

3. Create a new branch for your changes:

   ```
   git checkout -b MapReduceinPython/MapReduceinPython
   ```

4. Make your modifications and additions.

5. Commit your changes:

   ```
   git commit -m 
   ```

6. Push the changes to your forked repository:

   ```
   git push origin MapReduceinPython/MapReduceinPython
   ```

7. Open a pull request on the original repository, explaining your changes and why they should be merged.

8. Wait for feedback or approval on your pull request. Make any requested changes if necessary.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify

 the code according to your needs.

## Acknowledgments

The implementation of the MapReduce algorithm in this project is based on the concepts and principles introduced by Google in their original research paper: "MapReduce: Simplified Data Processing on Large Clusters" by Jeffrey Dean and Sanjay Ghemawat.

Publication link - https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf

 
