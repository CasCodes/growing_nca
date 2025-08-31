# Growing neural cellular automata
> Trying to implement Mordvintsev, et al., "Growing Neural Cellular Automata", Distill, 2020. in order to learn about neural cellular automata
> See their amazing explanation at https://distill.pub/2020/growing-ca/

In this small project I try to implement the growing NCA as proposed by Mordvintsev, et al. 

For simplicities sake I only used 8 channels, with 4 being hidden channels. 
To learn the update rules this implementation uses a 1x1 convolution which takes a 24-dimensional "percieved" vector for each cell, expands it to 32-dimensions and then compresses it to 8 dimensions (channels) which is the cell state for the next epoch.

The full "TUM" logo appears to be a bit too detailed for this simplified version of the growing-ca, but at least it managed to learn the "T" quite well:


<img width="200" alt="Screenshot 2025-08-31 at 19 50 04" src="https://github.com/user-attachments/assets/2897a9e2-1fbd-4f17-b1c1-9fb9022d1efd" />

<img height="200" alt="Screenshot 2025-08-31 at 19 47 27" src="https://github.com/user-attachments/assets/d1b3548f-9050-45ab-a0ce-a4a110649e1d" />

(left: target image "T", right: snapshot of the NCA during training)

Here you can see a pretty little gif of the NCA trying to learn the target image over around 1500 epochs:
![nca_evolution_1500epochs_8channels](https://github.com/user-attachments/assets/0b92f731-0edf-4521-b692-2ee95636d7df)
