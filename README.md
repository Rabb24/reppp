# reppp

import pandas as pd
import pyarrow.parquet as pq

# Lista plików Parquet, które chcesz sprawdzić
files = [
    'admin_oper_23_24.parquet',
    'client_oper.parquet',
    'history_client_oper_23_24.parquet'
]

# Funkcja do wyświetlenia nagłówków tabel
def show_columns(file_path):
    # Wczytaj plik Parquet do DataFrame
    df = pd.read_parquet(file_path)
    # Wyświetl kolumny
    print(f"Columns in {file_path}:")
    print(df.columns.tolist())
    print()

# Przejdź przez każdy plik i wyświetl jego nagłówki
for file in files:
    show_columns(file)
