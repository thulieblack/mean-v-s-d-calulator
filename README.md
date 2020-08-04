# mean-v-s-d-calulator

import numpy as np

calculations = {}
def calculate (the_list):
    if len(the_list) != 9:
        
        matrix = np.reshape(the_list,(3,3))
        
        mu = dict({'axis_0':np.mean(matrix,axis=0),'axis=1':np.mean(matrix,axis=1),'flattened':np.mean(matrix)})
        var_= dict({'axis_0':np.var(matrix,axis=0),'axis=1':np.var(matrix,axis=1),'flattened':np.var(matrix)})
        std_= dict({'axis_0':np.std(matrix,axis=0),'axis=1':np.std(matrix,axis=1),'flattened':np.std(matrix)})
        max_= dict({'axis_0':np.max(matrix,axis=0),'axis=1':np.max(matrix,axis=1),'flattened':np.max(matrix)})
        min_= dict({'axis_0':np.min(matrix,axis=0),'axis=1':np.min(matrix,axis=1),'flattened':np.min(matrix)})
        sum_= dict({'axis_0':np.sum(matrix,axis=0),'axis=1':np.sum(matrix,axis=1),'flattened':np.sum(matrix)})
        
        calculations = {'mean': [mu], 'varience': [var_],'standard deviation': [std_],'max': [max_],'min': [min_],'sum': [sum_]}
        
        return calculations
    else:
        print('must contain nine numbers')
        the_list = [0,1,2,3,4,5,6,7,8,9]
calculate(the_list)
the_list = [0,1,2,3,4,5,6,7,8]
calculate(the_list)
