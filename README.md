            Project Definition

In this project we aim to predict the stock prices of a
company using advanced Deep Learning model, GRU.
Long Short-Term Memory (LSTM) and Gated Recurrent
Unit(GRU) is a type of recurrent neural network (RNN)
that has been proven to be effective in modeling
sequential data, making it a popular choice for stock price
prediction. In this project, we will use GRU to predict the
stock prices of a large multinational Organization ,
Microsoft.

               Why do we need GRU?

Recurrent Neural Networks (RNNs) are a popular class of neural
network models used in time series forecasting due to their ability
to capture temporal dependencies and handle sequences of
arbitrary length. However, RNNs also have some limitations
when it comes to time series forecasting, including:
1.Vanishing gradients: RNNs are trained using backpropagation
through time (BPTT), which can suffer from the vanishing
gradients problem when the gradients become too small to be
useful for learning. This can make it difficult for RNNs to learn
long-term dependencies in the data.
2.Memory limitations: RNNs have a fixed memory capacity, which
limits their ability to remember long-term patterns in the data.
This can be a problem for time series with long-term
dependencies, such as those with seasonality or cyclic patterns.

              Detailed Explanation of GRU

To solve the vanishing gradient problem of a standard RNN,
GRU uses, so-called, update gate and reset gate. Basically,
these are two vectors which decide what information should
be passed to the output. The special thing about them is that
they can be trained to keep information from long ago,
without washing it through time or remove information which
is irrelevant to the prediction.

Reset gate: r_t = sigmoid(W_r * [h_{t-1}, x_t])

Update gate: z_t = sigmoid(W_z * [h_{t-1}, x_t])

Candidate hidden state: h_t’

= tanh(W_h * [r_t * h_{t-1}, x_t])

Hidden state: h_t = (1 – z_t) * h_{t-1} + z_t * h_t’

         Comparison between time series 
       forecasting techniques LSTM and GRU

GRUs have a simpler architecture compared to LSTMs. GRUs have two 
gates (update and reset gates) combined with a candidate hidden state, 
whereas LSTMs have three gates (input, forget, and output gates) 
combined with a memory cell. The reduced number of gates in GRUs
makes them computationally less expensive and easier to train.
Due to their simpler structure, GRUs are generally faster to train and
require less computational resources compared to LSTMs. This can be
particularly advantageous when dealing with large-scale datasets or
resource-constrained environments.
While LSTMs have been the dominant choice for many years and are
well-established in various applications, recent research has shown that
GRUs can perform comparably to LSTMs in many tasks. In certain cases,
GRUs have been found to converge faster and achieve similar or even
better results than LSTMs.

            Accuracy Score of The GRU Model

Explained_varience =1 – var(y – y')/var(y)

Train data explained variance regression score: 0.9689423177287514

Test data explained variance regression score: 0.9638433729653627

R squared score

Train data R2 score: 0.9689301236073743

Test data R2 score: 0.9606193540372692
