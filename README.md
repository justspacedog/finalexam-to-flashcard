# finalexam-to-flashcard

This is based on the work of [Nikolas](https://greek.doctor) [https://github.com/greekdoctor/finalexam-questioncollector-js](https://github.com/greekdoctor/finalexam-questioncollector-js), but in this version it is easier to import it into a flashcard app with multiple choice question (MCQ) support. It is not completely error-free, not least because some regex commands do not work (please use a separate text editor for this - see comments in the source code).

At the end of studies in general medicine, dentistry, and pharmacology in Hungary, a written national "final exam" must be taken. This is a multiple choice question-based exam, and the questions are provided to the students ahead of time at the website finalexam.hu. However, on the website the questions are displayed 20 at a time, the website logs you out pretty fast, logging in with my password manager is not possible, and at the time of writing (may 2023) there are 3972 questions for the german program. Having the questions in a text-based format allows for printing and easier creation of flashcards, etc.

This short javascript snippet takes each page of 20 questions, copies the question stem and explanation for each question, and creates a blob textfile from which the questions can be copy pasted into a .tsv document, which can then be imported in an App like [Flashcard Hero](http://flashcardhero.com). Question/Answer are separated by `tab` and text is quoted with `double quotation marks`. You can see an example here:
![carbon code example](https://github.com/justspacedog/finalexam-to-flashcard/raw/main/carbon.png)

The Answer itself is not in the file, since the above mentioned app is capable of MCQ, so you can just select the answer options and select the right answer. Since I have used the German questions you have to adjust some things when you want to use it for the English or Hungarian questions.

# Usage

1. Log into finalexam.hu (creating a user is free and does not require proving student status)
2. Open the question list and navigate to one of the pages with questions.
3. Copy paste the script into the console (right click -> inspect -> console (in chromium-based browsers) and execute it
4. A new tab will open with the questions from that page. Copy and paste them to a separate document (and add a newline (press enter))
5. Navigate to the next page with questions. Rerun the script (arrow up + enter reruns the previous command)
6. Repeat until finished
