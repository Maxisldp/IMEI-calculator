# IMEI-calculator
# My first python project to develope a IMEI calculator

imei = str(input ("Give me the imei number: "))
odd_imei = 0
even_imei = 0
last_digit =0

#calculate odd number
for a in range (0, 14, 2):
        a_imei = int(imei[a])
        odd_imei += a_imei
        
#calculate even number
for b in range (1, 14, 2):
        b_imei = int(imei[b])*2
        if b_imei > 9:
                str_imei = str(b_imei)
                c_imei = int(str_imei[0])
                d_imei = int(str_imei[1])
                b_imei = c_imei + d_imei
        even_imei += b_imei

#calculate last digit
for x in range (0, 10, 1):
        last_digit = (odd_imei + even_imei + x)%10
        if last_digit%10 == 0:
                print("the last digit is " + str(x))
                print("IMEI is " + str(imei)+ str(x))

        
