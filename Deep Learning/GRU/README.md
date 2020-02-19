**GRU**: GRU’s got rid of the cell state and used the hidden state to transfer information. It also only has two gates, a reset gate and update gate.
1) Reset Gate - The reset gate is another gate is used to decide how much past information to forget.
2) Update Gate - It acts similar to the forget and input gate of an LSTM. It decides what information to throw away and what new information to add.

GRU’s has fewer tensor operations; therefore, they are a little speedier to train then LSTM’s. 
