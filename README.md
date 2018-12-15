# Human Identifier
Contains sample files for training [OpenCV's cascade classifier](https://docs.opencv.org/3.4/dc/d88/tutorial_traincascade.html) to detect human outlines.

The samples are in-game screenshots from [Counter-Strike](https://en.wikipedia.org/wiki/Counter-Strike) 1.6.

# Contents
#### person.vec:

A summarized file containing data from 1280 positive samples 

#### neg:

Contains 1047 negative samples

#### bg.txt:

Lists all the negative sample files in the _neg_ directory

#### output

The location of the trained classifier

# Usage
Copy all the files to same location as the _opencv_traincascade_ file and run the following command:
```python
opencv_traincascade -data output -vec person.vec -bg bg.txt -numPos 124 -numNeg 1047 -numStages 10 -h 64 -w 64
```
Feel free to tweak the last 5 parameters as per your requirements.

# Output Sample
![output sample](https://github.com/psyclone20/Human-Identifier/blob/master/output/sample.jpg)
