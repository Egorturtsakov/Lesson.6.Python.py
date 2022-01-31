# Lesson.6.Python.py

Задание 1:


import re

def reader(filename):

    regexp = r'\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}'
    
    with open(filename) as f:
    
        log = f.read()
        
        ips_list = re.findall(regexp, log)
        
    print(ips_list)
    
if __name__ == '__main__':

    reader('nginx_logs.txt')
    
    
    
 Задание 3:   
 
 
     $user_data = [
     
        'login' => '',
        
        'name' => '',
        
        'comments' => [
        
            [
            
                'post_id' => '',
                
                'comment_id' => '',
                
                'comment_text' => '',
                
            ],
            
            [
            
                'post_id' => '',
                
                'comment_id' => '',
                
                'comment_text' => '',
                
            ],
            
            [
            
                'post_id' => '',
                
                'comment_id' => '',
                
                'comment_text' => '',
                
            ],
            
        ],
        
    ];
    
    
    
Задание 6:  



import pickle


class MyClass():

    def __init__(self, param):
    
        self.param = param
        

def save_object(obj):

    try:
    
        with open("data.pickle", "wb") as f:
        
        
            pickle.dump(obj, f, protocol=pickle.HIGHEST_PROTOCOL)
            
    except Exception as ex:
    
        print("Error during pickling object (Possibly unsupported):", ex)
        

obj = MyClass(10)

save_object(obj)

