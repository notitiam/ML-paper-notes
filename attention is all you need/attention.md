- All images from Andrew Ng's Deeplearning.ai course 5: sequence models
- Existing language models (RNN + encoder-decoder)
    ![alt text](https://github.com/notitiam/ML-paper-notes/raw/master/attention%20is%20all%20you%20need/rnn.png "RNN")   
    - Problems:
        - Single vector representation by encoder
        - Network forgets for too long sequences
- Intuition of attention
    ![alt text](https://github.com/notitiam/ML-paper-notes/raw/master/attention%20is%20all%20you%20need/attention.png "RNN")   
    - Self attention
    - Look at smaller window of sequence and previous output to generate next output
    - `w<t,t'>` => weights of input sequence `t'` to look at for generating output `t`
    - weights generated by nerual network with input of previous output + activations
    - other types: for non NLP applications
    ![alt text](https://github.com/notitiam/ML-paper-notes/raw/master/attention%20is%20all%20you%20need/attention2.png "RNN")   

    ![alt text](https://github.com/notitiam/ML-paper-notes/raw/master/attention%20is%20all%20you%20need/attention-3.png "RNN")   
    
- Transformer model
    - From 'Attention is all you need' https://arxiv.org/abs/1706.03762
    ![alt text](https://github.com/notitiam/ML-paper-notes/raw/master/attention%20is%20all%20you%20need/transformer.png "RNN")   
    - Google brain
    - No encoder RNN, only attention
    - Feed forward arch, 
        - input => activation (hiddent state)
        - activation + prev output => output
    - Multi head attention
        - For each input word, get `h` different attentions (`h` = 8 for transformer)
        - Allows focussing on different part of sentence
    - Position embedding in output
        - Encode position explicity (no recurrence)
    - Masked attention in decoder
        - Prevent looking at future output at training
    - Attention in encoder as well as decoder
    
    ![alt text](https://github.com/notitiam/ML-paper-notes/raw/master/attention%20is%20all%20you%20need/attention-4.png "RNN")   
    
