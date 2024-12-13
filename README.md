Boolean Search on Reviews

This project performs searches on Amazon customer reviews using three differnt methods.

The first uses basic boolean search using AND on all aspects and opinions.
The second uses the previous boolean search but uses ratings to enhance the results.
The third identifies reviews where aspects and opinions co-occur in specific sentences.

Before running the program you need some required packages such as pandas, and nltk.
I made it so the program will download punkt, punkt_tab, and stopwords if you don't already have those installed.
The corpus which in this case would be review_segment needs to a pkl format as well.

To run the program it requires at least two aspect terms, a opinion term, and the method of choice.

In the terminal you must enter the script this format:

python boolean_search.py --aspect1 aspectTerm1 --aspect2 aspectTerm2 --opinion opinionTerm --method methodChoice
you can use py, python, or even python3, it just depends on your system.

For two worded opinion terms like "click problem" you would need to add double apostrophes or "air quotes" to the script.

For example:
python boolean_search.py --aspect1 aspectTerm1 --aspect2 aspectTerm2 --opinion "opinionTerm" --method methodChoice

The three method choices you can choose from are "baseline", "BooleanRatingSearch", and "OpinionOrientation".

So if I wanted to put a query in for audio quality:poor using the OpinionOrientation method I would enter:
py boolean_search.py --aspect1 audio --aspect2 quality --opinion poor --method OpinionOrientation

The program will make a posting list if it doesn't already have one inside the code folder and then run the method.After
it is done it will create an output folder if it hasn't been made and then put the output in the form of a pickle file 
inside the output folder.

Important Note: The program is meant to be used in this folder format WorkspaceFolder[(code), (output)] where the code folder will have posting_list and the 
dataset in this case reviews_segment.pkl inside the folder so it can properly get and read the information as needed.
    Folder/
    ├── code/
    │   ├── boolean_search.py
    │   ├── reviews_segment.pkl
    │   └── posting_list.pkl
    ├── output/ (created automatically if it does not exist)
