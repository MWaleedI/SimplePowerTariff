hourly_consumption = [0] * 24
on_peak_units = 0
off_peak_units = 0
print("*** WELCOME TO POWER CONSUMPTION CALCULATOR  ***")
for number in range(24):
    hourly_consumption[number] = input(
        f"Please Enter your Power COnsumption for Hour No. {number+1} : ")
    if number <= 16:
        off_peak_units += int(hourly_consumption[number])
    else:
        on_peak_units += int(hourly_consumption[number])
total_bill = (on_peak_units * 60) + (off_peak_units * 45)
print(f"Total Bill Amount: PKR{total_bill} : ")
print(f"Total On-Peak Units Consumed: {on_peak_units}")
print(f"Total Off-Peak Units Consumed: {off_peak_units}")
