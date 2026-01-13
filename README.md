# Employee-Salary-Slip-Program-Using-Functions-in-Python
def calculate_salary(basic):
    hra = basic * 0.20
    da = basic * 0.10
    ta = basic * 0.05
    gross_salary = basic + hra + da + ta

    pf = basic * 0.12
    tax = basic * 0.05
    total_deductions = pf + tax

    net_salary = gross_salary - total_deductions

    return hra, da, ta, gross_salary, pf, tax, net_salary


def print_salary_slip(emp_id, emp_name, basic):
    hra, da, ta, gross, pf, tax, net = calculate_salary(basic)

    print("\n--------- SALARY SLIP ---------")
    print(f"Employee ID   : {emp_id}")
    print(f"Employee Name : {emp_name}")
    print(f"Basic Salary  : {basic:.2f}")
    print("--------------------------------")
    print(f"HRA (20%)     : {hra:.2f}")
    print(f"DA (10%)      : {da:.2f}")
    print(f"TA (5%)       : {ta:.2f}")
    print("--------------------------------")
    print(f"Gross Salary  : {gross:.2f}")
    print("--------------------------------")
    print(f"PF (12%)      : {pf:.2f}")
    print(f"Tax (5%)      : {tax:.2f}")
    print("--------------------------------")
    print(f"Net Salary    : {net:.2f}")
    print("--------------------------------")


# Main Program
emp_id = 101
emp_name = "Rahul"
basic_salary = 20000

print_salary_slip(emp_id, emp_name, basic_salary)
--------- SALARY SLIP ---------
Employee ID   : 101
Employee Name : Rahul
Basic Salary  : 20000.00
--------------------------------
HRA (20%)     : 4000.00
DA (10%)      : 2000.00
TA (5%)       : 1000.00
--------------------------------
Gross Salary  : 27000.00
--------------------------------
PF (12%)      : 2400.00
Tax (5%)      : 1000.00
--------------------------------
Net Salary    : 23600.00
--------------------------------

