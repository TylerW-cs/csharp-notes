The brief:

Ask the user for the total bill amount, the tip percentage they want to leave, and how many people are splitting it — using Console.ReadLine() three times, with Console.WriteLine() prompts before each.

Calculate the tip amount (bill × tip% ÷ 100), the grand total (bill + tip), and the amount each person owes (total ÷ number of people).

Print all three results back out using string interpolation, e.g. $"Each person owes: {perPerson}".

Add an if/else-if chain that gives feedback based on the tip percentage entered — something like "That's a low tip" if under 10%, "Standard tip" if 10–20%, "Very generous!" if over 20%.