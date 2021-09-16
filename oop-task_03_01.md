class student:
    def __init__(self,name):
        self.name = name
     
class studentresultinfo(student):
    def __init__(self,name,total_marks):
        self.total_marks = total_marks
        student.__init__(self,name)

    def read(self):
        self.reg = (int)(input("Enter roll no : "))
        self.age = (int)(input("Enter your age : "))
        self.gender = input("Enter your gender : ")
        self.branch = input("Enter your branch : ")
        self.sem = (int)(input("Enter your sem : "))
        self.percentage = (self.total_marks)/5
        self.grade = input("Enter your Grade : ")  
    def display(self):
        print("Name : {}\nREG = {}\nAGE = {}\nGENDER = {}\nBRANCH = {}\nSEM = {}\nTOTAL_MARKS = {}\nPERCENTAGE = {}\nGRADE = {}\n".format(self.name,self.reg,self.age,self.gender,self.branch,self.sem,self.total_marks,self.percentage,self.grade)) 
    
    
student1 = student("jayant")

student1  = studentresultinfo("jayant",446)
student1.read()
student1.display()
