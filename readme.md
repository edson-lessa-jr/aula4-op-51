# 🔢 Algoritmos de Ordenação em C - Bubble Sort, Selection Sort e Insertion Sort

Este projeto implementa e demonstra três algoritmos básicos de ordenação em **C**:
- 🟢 **Bubble Sort**
- 🔵 **Selection Sort**
- 🔴 **Insertion Sort**

O código possui um **menu interativo**, permitindo ao usuário escolher qual algoritmo executar.

---

## 📂 **Estrutura do Projeto**
O código está organizado em **pastas modulares**, separando cada algoritmo:  
📦 ordenacao-em-c  
├── 📂 01-bubblesort  
│ ├── bubblesort.c  
│ ├── bubblesort.h  
├── 📂 02-selectionsort  
│ ├── selectionsort.c  
│ ├── selectionsort.h  
├── 📂 03-insertsort  
│ ├── insertionsort.c  
│ ├── insertionsort.h  
├── .gitignore  
├── main.c  
└── README.md  

📌 **Explicação dos arquivos**:
- 📁 **`01-bubblesort/`** → Implementação do Bubble Sort.
- 📁 **`02-selectionsort/`** → Implementação do Selection Sort.
- 📁 **`03-insertsort/`** → Implementação do Insertion Sort.
- 📝 **`main.c`** → Menu interativo para chamar cada algoritmo.

---

## 🚀 **Compilação e Execução**
Para compilar e rodar o programa, use os seguintes comandos:

```sh
gcc main.c 01-bubblesort/bubblesort.c 02-selectionsort/selectionsort.c 03-insertsort/insertionsort.c -o ordenacao
./ordenacao
```

🎮 Funcionalidades
O programa apresenta um menu interativo, onde o usuário pode escolher qual algoritmo executar:
```
=== MENU DE ORDENACAO ===
1 - Executar Bubble Sort
2 - Executar Selection Sort
3 - Executar Insertion Sort
0 - Sair
```

📌 Cada algoritmo gera um array aleatório de 10 números e o ordena.

🛠 Implementação dos Algoritmos  
1️⃣ Bubble Sort  
📌 Descrição: Compara elementos adjacentes e troca se estiverem fora de ordem.  
📌 Complexidade: O(n²)  
```
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

```

2️⃣ Selection Sort  
📌 Descrição: Seleciona o menor elemento e o coloca na posição correta.  
📌 Complexidade: O(n²)

```
void selectionSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        int minIndex = i;
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }
        int temp = arr[i];
        arr[i] = arr[minIndex];
        arr[minIndex] = temp;
    }
}

```
3️⃣ Insertion Sort  
📌 Descrição: Insere cada elemento na posição correta, como cartas de baralho.  
📌 Complexidade: O(n²), mas eficiente para listas pequenas.  

```
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}

```
📌 Exemplo de Saída  
```
=== MENU DE ORDENACAO ===
1 - Executar Bubble Sort
2 - Executar Selection Sort
3 - Executar Insertion Sort
0 - Sair
Escolha uma opcao: 1

Gerando lista de numeros aleatorios...
Array antes da ordenacao: 83 12 57 41 99 3 28 75 90 10
Array apos a ordenacao: 3 10 12 28 41 57 75 83 90 99
```
📚 Sobre o Autor  
👨‍🏫 Professor: Edson Orivaldo Lessa Junior  
📌 Disciplina: Pesquisa e Ordenação de Dados  
📌 Ciclo: 51  

Este projeto foi criado como material didático para ilustrar algoritmos básicos de ordenação em C.  

📌 Autor: [Edson Orivaldo Lessa Junior]  
📌 Contato: [Seu E-mail ou GitHub]  

📝 Licença  
Este projeto está sob a licença MIT. Use e modifique livremente!  

---

### **📌 O que este README cobre?**
✔ **Explica a estrutura do projeto**  
✔ **Fornece instruções de compilação e execução**  
✔ **Lista as funcionalidades do menu interativo**  
✔ **Explica cada algoritmo de ordenação com código**  
✔ **Mostra um exemplo real de saída**  
✔ **Inclui informações sobre o autor e a disciplina**

🚀 **Agora seu repositório no GitHub está bem documentado!** 🚀  
Se precisar de ajustes ou quiser incluir mais informações, me avise! 😊







