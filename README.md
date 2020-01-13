# Filternet

FilterNet is a ensemble neural network model used for time series analysis. It is comprised of a 1D convolutional neural network and fast.ai's MixedInputModel. An example of the network implemented in PyTorch is located in filternet.py and provides the model class along with its corresponding dataset class. Links to the abstract, slides, and video of our presentation at PyData Los Angeles 2018 will be provided below.

This 1D convolutional neural network (CNN) was inspired by the traditional use of filters in discrete time signal processing. While developed independently, it closely resembles the findings described in the WaveNet paper by Borovykh et al. While the 1D CNN performed well on its own, datasets can have a lot of context associated with them (hour of day, day of week, etc.) which the 1D CNN alone is unable to handle. We utilized fastai's MixedInputModel, which has been used successfully for tabular data, to include learnings on the context portion of our datasets. The two neural networks are combined using a final regression layer and were found to compliment each other. In testing, the resulting ensemble model outperformed one of our current best production time series models (TBATS).


Contributing authors:

Jeff Roach (Data Scientist at System1)
Nathan Janos (Chief Data Officer at System1)
For more information about System1, please visit: www.system1.com
