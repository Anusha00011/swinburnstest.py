# swinburnstest.py
swinburn test

# Swinburne's Test of DC Machine

V = float(input("Enter supply voltage (V): "))
I0 = float(input("Enter no-load current (A): "))
Ra = float(input("Enter armature resistance (ohm): "))
IL = float(input("Enter load current (A): "))

# No-load losses
Armature_loss = I0**2 * Ra
Input_power = V * I0
Constant_losses = Input_power - Armature_loss

# Load condition
Armature_copper_loss = IL**2 * Ra
Output_power = V * IL - Armature_copper_loss - Constant_losses
Input_load_power = V * IL

# Efficiency
Efficiency = (Output_power / Input_load_power) * 100

print("\n--- Swinburne's Test Results ---")
print("Constant Losses =", Constant_losses, "W")
print("Armature Copper Loss =", Armature_copper_loss, "W")
print("Output Power =", Output_power, "W")
print("Efficiency =", Efficiency, "%")