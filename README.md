# Japanese Language Difficulty Score

This project provides a tool to calculate the difficulty score of Japanese text based on the complexity of Kanji characters used. The difficulty is determined by the number of strokes in each Kanji character, with more complex characters contributing more to the overall difficulty score.

## Features

- **Tokenize Japanese Text**: Uses MeCab to tokenize Japanese text.
- **Kanji Stroke Data**: Loads Kanji stroke data from a CSV file.
- **Difficulty Calculation**: Computes a difficulty score based on the top 5% most complex Kanji characters.
- **Visualization**: Plots the distribution of Kanji strokes and difficulty scores.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/japanese-language-difficulty-score.git
   cd japanese-language-difficulty-score
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Download and install [MeCab](https://taku910.github.io/mecab/).

## Usage

1. Prepare a text file containing Japanese text. For example, `testCases.txt`.

2. Run the Jupyter Notebook `difficulty_score_kenji.ipynb` to calculate the difficulty score of the provided text. The main functions are:

   - **is_kanji(char)**: Checks if a character is a Kanji.
   - **load_data()**: Loads Kanji stroke data from a CSV file.
   - **calculate_difficulty_score(japanese_text)**: Calculates the difficulty score for the given Japanese text.
   - **tokenize_japanese_text(text)**: Tokenizes Japanese text using MeCab.
   - **calculate_top_percent_threshold(strokes_data, top_percent)**: Calculates the stroke threshold for the top percentage of Kanji characters.
   - **get_number_of_strokes(kanji_char, strokes_data)**: Retrieves the number of strokes for a given Kanji character.
   - **plot_strokes_distribution(strokes_data)**: Plots the distribution of strokes in Kanji characters.
   - **plot_difficulty_pie_chart(difficulty_stats)**: Plots a pie chart of the difficulty distribution in Japanese text.

3. Example usage:
   ```python
   # Specify the file path
   file_path = 'testCases.txt'

   # Open the file with the appropriate encoding (UTF-8)
   with open(file_path, 'r', encoding='utf-8') as file:
       # Read the content of the file
       japanese_text = file.read()

   # Calculate difficulty score
   difficulty_score = calculate_difficulty_score(japanese_text)
   print("Difficulty Score:", difficulty_score)
   ```

## Data

- `Kanji_char.csv`: A CSV file containing Kanji characters and their corresponding stroke counts.

## Visualization

- The notebook provides functions to visualize the stroke distribution and the difficulty score distribution of the text.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License.
