### Instructions for running the Stanford NER software as a server and then reaching it via Python.

-- Download Stanford NER from here: http://nlp.stanford.edu/software/CRF-NER.shtml .  I used version 3.4
-- Unpack it
-- cd into its directory
-- Download the Python NER which is a Python client for Stanford NER: https://pypi.python.org/pypi/ner/#downloads  I was using 0.1
-- Install that by running 'python setup.py install'
-- To run the NER server, now back in the Stanford NER directory, run: java -mx1000m -cp stanford-ner.jar edu.stanford.nlp.ie.NERServer -loadClassifier classifiers/english.muc.7class.distsimrf.ser.gz -port 8080 -outputFormat inlineXML 
-- Now open a python prompt with 'python':
>> import ner
>> tagger = ner.SocketNER(host='localhost', port=8080)
>> tagger.get_entities("University of California is located in California, United States")

That will return: {'ORGANIZATION': ['University of California'], 'LOCATION': ['California', 'United States']}

 
