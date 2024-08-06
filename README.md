# reppp

import pandas as pd

def top_15_most_frequent(file_path, column_name):
    # Wczytanie danych z pliku CSV
    df = pd.read_csv(file_path)
    
    # Zliczanie wystąpień wartości w wybranej kolumnie
    value_counts = df[column_name].value_counts()
    
    # Wybieranie 15 najczęściej powtarzających się wartości
    top_15 = value_counts.head(15)
    
    return top_15

# Ścieżka do pliku CSV i nazwa kolumny
file_path = 'path_to_your_file.csv'
column_name = 'your_column_name'

# Wywołanie funkcji i wyświetlenie wyników
top_15_values = top_15_most_frequent(file_path, column_name)
print(top_15_values)
