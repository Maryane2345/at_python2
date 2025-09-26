import sqlite3
from datetime import datetime

banco = sqlite3.connect("tarefas.db")
sql = banco.cursor()

sql.execute("""
CREATE TABLE IF NOT EXISTS tarefas (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    titulo TEXT NOT NULL,
    descricao TEXT,
    prioridade TEXT,
    concluida INTEGER DEFAULT 0,
    criada_em TEXT
)
""")
banco.commit()

def nova_tarefa():
    titulo = input("Título: ")
    descricao = input("Descrição: ")
    prioridade = input("Prioridade (baixa, média, alta): ")
    criada_em = datetime.now().strftime("%d/%m/%Y %H:%M:%S")

    sql.execute(
        "INSERT INTO tarefas (titulo, descricao, prioridade, criada_em) VALUES (?, ?, ?, ?)",
        (titulo, descricao, prioridade, criada_em)
    )
    banco.commit()
    print("✔ Tarefa salva!")

def mostrar_tarefas():
    print("\nExibir (1) Todas | (2) Por prioridade | (3) Por status")
    escolha = input("Opção: ")

    if escolha == "2":
        prio = input("Qual prioridade (baixa/média/alta): ")
        sql.execute("SELECT * FROM tarefas WHERE prioridade = ?", (prio,))
    elif escolha == "3":
        st = int(input("Status (0 = pendente | 1 = concluída): "))
        sql.execute("SELECT * FROM tarefas WHERE concluida = ?", (st,))
    else:
        sql.execute("SELECT * FROM tarefas")

    tarefas = sql.fetchall()
    print("\n------ TAREFAS ------")
    for t in tarefas:
        status = "Concluída" if t[4] == 1 else "Pendente"
        print(f"[{t[0]}] {t[1]} | {t[3]} | {status} | Criada em: {t[5]}")
    print("----------------------\n")

def finalizar_tarefa():
    tarefa_id = input("ID da tarefa a concluir: ")
    sql.execute("UPDATE tarefas SET concluida = 1 WHERE id = ?", (tarefa_id,))
    banco.commit()
    print("✔ Concluída com sucesso!")

def remover_tarefa():
    tarefa_id = input("ID da tarefa a excluir: ")
    sql.execute("DELETE FROM tarefas WHERE id = ?", (tarefa_id,))
    banco.commit()
    print("✘ Tarefa removida!")

def menu():
    while True:
        print("\n==== TO-DO LIST ====")
        print("1 - Nova tarefa")
        print("2 - Listar tarefas")
        print("3 - Concluir tarefa")
        print("4 - Excluir tarefa")
        print("0 - Sair")
        opc = input("Escolha: ")

        if opc == "1":
            nova_tarefa()
        elif opc == "2":
            mostrar_tarefas()
        elif opc == "3":
            finalizar_tarefa()
        elif opc == "4":
            remover_tarefa()
        elif opc == "0":
            print("Até logo!")
            break
        else:
            print("Opção inválida!")

if __name__ == "__main__":
    menu()
    banco.close()