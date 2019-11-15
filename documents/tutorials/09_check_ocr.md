## How to Check Accuracy of OCR Model

Once you have trained Kraken, you will want to check the accuracy of your model outside the training set (since the error rate Kraken provides is based on the training set).

[ocrevalUAtion](https://github.com/impactcentre/ocrevalUAtion) is a useful tool for checking the accuracy of your OCR model.

1. Follow the instructions on the ocrevalUAtion's GitHub to download the program (you may have to install the most recent version of Java)

2. Place your OCR output and ground truth in text files in a single folder

3. In the same folder, create a blank .html file (this will be your output)

4. Using the ocrevalUAtion's interface, select text files of your ground truth and the OCR's output. Click "Generate report" and select the blank .html file as your output

5. Open the .html file to access the report
