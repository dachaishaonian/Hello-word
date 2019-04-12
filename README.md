# Hello-word
Just another repository
import torch
from torch.autograd import Variable
import numpy as np
import matplotlib.pyplot as plt

torch.manual_seed(2017)

<torch._C.Generator at 0x108f3c5f0>

with open('./data.txt','r') as f:
     data_list=[i.split('\n')[0].split(',') for i in f.readlines()]
     data=[(float(i[0]),float(i[2])) for i in data_list]
     
     x0_max=max([i[0] for i in data])
     x1_max=max([i[1] for i in data])
     data=[(i[0]/x0_max,i[1]/x1_max,i[2] for i in data]
     
     x0=list(filter(lambda x:x[-1]==0.0,data))
     x1=list(filter(lambda x:x[-1]==1.0,data))
     
     plot_x0=[i[0] for i in x0]
     plot_y0=[i[1] for i in x0]
     plot_x1=[i[0] for i in x1]
     plot_y1=[i[1] for i in x1]
     
     plt.plot(plot_x0,plot_y0,'ro',label='x_0'
     plt.plot(plot_x1,plot_y1,'bo',label='x_1'
     plt.legend(loc='best')
     
     <matplotlib.legend at 0x108137c50>
