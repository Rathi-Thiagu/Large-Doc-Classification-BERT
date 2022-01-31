Resource: 
       Google colab 
	   Hardware accelerator: GPU 
	   Memory : High RAM 
	   
This is a data-based approach to extract contextualized word embeddings for documents with more than 512 tokens using     Google's BERT (Maximum input token length for BERT is 512) 
The approach involves splitting each input document into chunks of 250 words(50 overlapping words), getting the word embeddings for the chunks from BERT, and combining them using dimension reduction techniques like Autoencoders, PCA, KPCA, mean of chunks, mean of high variance chunks to get a final word embedding for the classification task using LSTM and Transformers.
It is observed that for documents with 2000 words, mean of high variance chunks, Autoencoder approaches improved the classification test accuracy from 0.81(without chunks) to 0.89.

Two Datasets are used : 
	Consumer complaints (can be download from:https://www.kaggle.com/ashwinik/consumer-complaints-financial-products  )
	Supreme court decisions (can be downloaded from Textacy python library)

Code Reference: 
	BERT Embedding extraction: 
	https://medium.com/@armandj.olivares/using-bert-for-classifying-documents-with-long-texts-5c3e7b04573d

