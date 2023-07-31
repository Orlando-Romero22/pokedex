# pokedex
import requests
import json
def get_pokemon():

    pokemon = input("Ingrese el pokemon que requiera consultar:")

    try:

        A = requests.get(f"https://pokeapi.co/api/v2/pokemon/{pokemon}")
        A.raise_for_status
        data = A.json()

    except requests.exceptions.RequestException as e:
        print("Se produno un error al realizar esta solicitud", e)
    except ValueError as e:
        print("Error al analizar la solicitud", e)
    except Exception as e:
        print("Error inesperado", e)  
    else:
        print("La API se ejecuto correctamente") 
        json.dump(data, archivo)     
    finally:
        print("Gracias por utilizar este codigo")


if __name__ == "__main__":
    get_pokemon()
