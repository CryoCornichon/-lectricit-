print("        	Calculateur de consommation électrique           											") 
device = input("Quel est l'appareil que vous allez utiliser ? ")
time_unite = input("Vous allez devoir dire le temps d'utilisation de votre " + device + " par jour, voulez vous le dire en minutes ou en heures ? ")
device_time = int(input("Quel est donc le temps moyen d'utilisation de votre " + device + " en " + time_unite + " par jour ? "))
watt = int(input("Quel est la consommation de votre " + device + " en watt ? "))
kwh_price = int(input("Quel est le prix de votre kwh en centimes ? "))
if time_unite != "minutes" or "en minutes" or "minute" or "en minute":
	device_time = device_time * 60
result = ((device_time / 60) * watt * 30 / 1000) *kwh_price / 100
round(result,2)
result_annual = result * 12
print("La consommation électrique mensuelle de votre " + device + " est de " + str(result) + " € " + ", la consommation annuelle est de " + str(result_annual) + " €.")
