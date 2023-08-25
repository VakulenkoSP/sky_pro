def calculate_bonus(years_of_service, sick_days):
  """
  Calculates the bonus for an employee.

  Args:
    years_of_service: The number of years the employee has worked for the company.
    sick_days: The number of sick days the employee took in the last year.

  Returns:
    The percentage of the employee's salary that they will receive as a bonus.
  """

  if years_of_service > 3:
    bonus_percent = 30
  elif years_of_service > 1.5:
    bonus_percent = 25
  elif years_of_service > 0:
    bonus_percent = 15
  else:
    bonus_percent = 0

  if sick_days == 0:
    bonus_percent += 3

  return bonus_percent


'''example'''

years_of_service = 10
sick_days = 10

bonus_percent = calculate_bonus(years_of_service, sick_days)

print(f"Иван получит премию в размере {bonus_percent}% от своей зарплаты.")
