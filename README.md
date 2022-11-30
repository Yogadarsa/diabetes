# diabetes
code for checking diabetes and data will be stored as a dataset
print("welcome to diabetes checking project answer all the following questions")
rows=[]
name=input("enter your name :")
rows.append(name)
age=int(input("enter your age:"))
rows.append(age)
sex=input("male or female or trans")
rows.append(sex)
thirsty_test=input("do you feel execive thirsty :")
if thirsty_test=="yes" or "no":
    y=input("do you feel execive hunger")
    if y=="yes" or "no":
        weight_test=input("unexplain weight loss is happened")
        if weight_test=="yes":
            main_test=input("slow heeling of cuts and wounds")
            if main_test=="yes":
                conf_ran="you may have diabetes please give blood test"
                print(conf_ran)
                rows.append(main_test)

        else:
            q=int("0")
            main_test="no problem"
            print(main_test)
            rows.append(q)

if main_test=="yes" :
    r=float(input("enter your test value in percentage:"))
    rows.append(r)
    if r<=5.7 :
        print("no problem")
        T=int("0")
        rows.append(T)
    elif r<=6.7 :
        print ("you may have perdiabetes")
        T=int("0.5")   #MAY COME
        rows.append(T)
    elif r>6.7:
        print("you are having diabetes")
        T=int("1")
        rows.append(T)

print(rows)


import csv
filename = "heart.csv"
with open(filename, 'a') as csvfile:
    csvwriter = csv.writer(csvfile)

    csvwriter.writerow(rows)
