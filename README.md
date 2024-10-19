Students-Exam-Score-Tracker
 Add a new student
    def add_student(self, name, scores):
        if name in self.students:
            print(f"Student {name} already exists.")
        else:
            self.students[name] = scores
            print(f"Added {name} with scores {scores}.")


 Update scores for an existing student
    def update_scores(self, name, new_scores):
        if name in self.students:
            self.students[name] = new_scores
            print(f"Updated scores for {name} to {new_scores}.")
        else:
            print(f"Student {name} does not exist.")


  Display all students and their scores
    def display_students(self):
        if not self.students:
            print("No students in the system.")
        else:
            for name, scores in self.students.items():
                print(f"Student: {name}, Scores: {scores}") 
                

  Get statistics (average, highest, lowest) for a student
    def student_statistics(self, name):
        if name in self.students:
            scores = self.students[name]
            average = sum(scores) / len(scores)
            highest = max(scores)
            lowest = min(scores)
            print(f"Statistics for {name}:")
            print(f"Average Score: {average}")
            print(f"Highest Score: {highest}")
            print(f"Lowest Score: {lowest}")
        else:
            print(f"Student {name} does not exist.")
            

   Remove a student
    def remove_student(self, name):
        if name in self.students:
            del self.students[name]
            print(f"Removed student {name}.")
        else:
            print(f"Student {name} does not exist.")
