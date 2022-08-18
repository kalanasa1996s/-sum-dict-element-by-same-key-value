# -sum-dict-element-by-same-key-value
 sum dictionaries element by same key value

     from collections import Counter


    vals =[
    
    {'id': 21, 'name': 'Kasun', 'Attendance_a': 50.0}, 
    {'id': 21, 'name': 'Kasun', 'Attendance_a': 500.0}, 
 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 70.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 80.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 900.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 50.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 40.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 5000.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 80.0}, 
    {'id': 22, 'name': 'Sasanka', 'Attendance_a': 5000.0}
    
    ]


    c = Counter()
    [c.update({d["id"]: d["Attendance_a"]}) for d in vals]
    result_of_Attendance_a_sum = [{"id": k, "Attendance_a": v} for k, v in c.items()]
    print(result_of_Attendance_a_sum)
    
    
  #output
  
    [{'id': 21, 'Attendance_a': 550.0}, {'id': 22, 'Attendance_a': 11220.0}]
   
  
