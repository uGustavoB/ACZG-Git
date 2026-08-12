
# Soluções — Command Line Challenges

## 1. Extrair o arquivo compactado

**Enunciado:** Extraia o arquivo `challenges.tar.gz`; você precisará de seu conteúdo para resolver parte dos desafios.

**Resposta:**

```bash
tar -xzf challenges.tar.gz
```

## 2. Entrar no diretório extraído

**Enunciado:** Altere o diretório de trabalho para `challenges`, criado ao extrair `challenges.tar.gz`.

**Resposta:**

```bash
cd challenges
```

## 3. Listar o conteúdo do diretório

**Enunciado:** Liste o conteúdo do diretório `challenges`.

**Resposta:**

```bash
ls
```

## 4. Criar o diretório `foo`

**Enunciado:** Crie um novo diretório chamado `foo`.

**Resposta:**

```bash
mkdir foo
```

## 5. Criar `foo/bar/1/2/3`

**Enunciado:** Crie um novo diretório no caminho `foo/bar/1/2/3`.

**Resposta:**

```bash
mkdir -p foo/bar/1/2/3
```

## 6. Remover `foo` e seu conteúdo

**Enunciado:** Remova o diretório `foo` e todo o seu conteúdo.

**Resposta:**

```bash
rm -rf foo
```

## 7. Exibir `Hello World`

**Enunciado:** Imprima o texto `Hello World`.

**Resposta:**

```bash
echo 'Hello World'
```

## 8. Criar `hello.txt` com o texto pedido

**Enunciado:** Crie um arquivo chamado `hello.txt` que contenha o texto `Hello World`.

**Resposta:**

```bash
echo 'Hello World' > hello.txt
```

## 9. Criar um arquivo vazio

**Enunciado:** Crie um arquivo vazio chamado `empty.txt`.

**Resposta:**

```bash
touch empty.txt
```

## 10. Remover `empty.txt`

**Enunciado:** Remova o arquivo `empty.txt`.

**Resposta:**

```bash
rm empty.txt
```

## 11. Segunda forma de criar um arquivo vazio

**Enunciado:** Encontre uma segunda forma de resolver o desafio 9.

**Resposta:**

```bash
: > empty.txt
```

## 12. Terceira forma de criar um arquivo vazio

**Enunciado:** Encontre uma terceira forma de resolver o desafio 9.

**Resposta:**

```bash
truncate -s 0 empty.txt
```

## 13. Copiar `hello.txt` para `goodbye.txt`

**Enunciado:** Copie `hello.txt` e dê à cópia o nome `goodbye.txt`.

**Resposta:**

```bash
cp hello.txt goodbye.txt
```

## 14. Renomear a cópia para `hello_copy.txt`

**Enunciado:** Renomeie `goodby.txt` para `hello_copy.txt`.

**Resposta:**

```bash
mv goodbye.txt hello_copy.txt
```

## 15. Demonstrar que os dois arquivos são idênticos

**Enunciado:** Comprove que o conteúdo de `hello.txt` e `hello_copy.txt` é idêntico.

**Resposta:**

```bash
diff -s hello.txt hello_copy.txt
```

## 16. Concatenar os dois arquivos

**Enunciado:** Concatene `hello.txt` e `hello_copy.txt` e armazene o resultado em `2_hellos.txt`.

**Resposta:**

```bash
cat hello.txt hello_copy.txt > 2_hellos.txt
```

## 17. Mostrar o caminho absoluto atual

**Enunciado:** Obtenha o caminho completo do diretório de trabalho atual (`challenges`).

**Resposta:**

```bash
pwd
```

## 18. Listar arquivos com permissões

**Enunciado:** Liste o conteúdo de `challenges`, como no desafio 3, exibindo as permissões de cada arquivo.

**Resposta:**

```bash
ls -l
```

## 19. Acrescentar texto a `restricted.txt`

**Enunciado:** Acrescente algum texto ao final de `restricted.txt`. É permitido fazer isso em duas etapas.

**Resposta:**

```bash
echo 'texto' >> restricted.txt
```

## 20. Executar `hello_executable`

**Enunciado:** Execute o programa `hello_executable`.

**Resposta:**

```bash
./hello_executable
```

## 21. Executar `challenge_20`

**Enunciado:** Execute o programa `challenge_20`. É permitido fazer isso em duas etapas.

**Resposta:**

```bash
chmod u+x challenge_20 && ./challenge_20
```

## 22. Compilar e executar o programa C

**Enunciado:** Compile e execute `compile_me.c`. É permitido fazer isso em duas etapas.

**Resposta:**

```bash
gcc compile_me.c -o compile_me && ./compile_me
```

## 23. Capturar toda a saída de `redirect`

**Enunciado:** Execute o programa `redirect` e colete toda a saída em um arquivo chamado `output.txt`.

**Resposta:**

```bash
./redirect > output.txt 2>&1
```

## 24. Mostrar data e hora

**Enunciado:** Obtenha a data e a hora atuais.

**Resposta:**

```bash
date
```

## 25. Mostrar os processos em execução

**Enunciado:** Exiba todos os processos em execução no computador.

**Resposta:**

```bash
ps aux
```

## 26. Mostrar o número de processadores/cores

**Enunciado:** Exiba o número de processadores/cores no computador.

**Resposta:**

```bash
nproc
```

## 27. Mostrar a versão do kernel

**Enunciado:** Descubra qual versão do kernel Linux está em execução.

**Resposta:**

```bash
uname -r
```

## 28. Encontrar a frase no conjunto de arquivos

**Enunciado:** Encontre, em `bunch_of_files/`, o arquivo que contém a string `You found the needle in the haystack!`.

**Resposta:**

```bash
grep -rlF 'You found the needle in the haystack' bunch_of_files
```

## 29. Mostrar as primeiras 25 linhas do CSV

**Enunciado:** Imprima as primeiras 25 linhas de `people.csv`.

**Resposta:**

```bash
head -n 25 people.csv
```

## 30. Mostrar as últimas 25 linhas do CSV

**Enunciado:** Imprima as últimas 25 linhas de `people.csv`.

**Resposta:**

```bash
tail -n 25 people.csv
```

## 31. Mostrar somente as diferenças entre dois arquivos

**Enunciado:** Exiba somente as diferenças entre `greeting1.txt` e `greeting2.txt`.

**Resposta:**

```bash
diff greeting1.txt greeting2.txt
```

## 32. Escrever uma mensagem, esperar e escrever outra

**Enunciado:** Imprima `Hello`, espere 5 segundos e então imprima `world!`.

**Resposta:**

```bash
echo 'Hello'; sleep 5; echo 'world'
```

## 33. Criar 1 MB de zeros

**Enunciado:** Crie um arquivo de 1 MB preenchido com zeros.

**Resposta:**

```bash
dd if=/dev/zero of=zeros.bin bs=1M count=1
```

## 34. Criar 2 MB de dados aleatórios

**Enunciado:** Crie um arquivo de 2 MB preenchido com dados aleatórios.

**Resposta:**

```bash
dd if=/dev/urandom of=arquivo.bin bs=1M count=2
```

## 35. Contar as linhas de `README.txt`

**Enunciado:** Conte o número de linhas de `README.txt`.

**Resposta:**

```bash
wc -l README.txt
```

## 36. Exibir `README.txt` da última linha para a primeira

**Enunciado:** Exiba o conteúdo de `README.txt` em ordem inversa, da última linha para a primeira.

**Resposta:**

```bash
tac ../README.txt
```

## 37. Exibir os sobrenomes do CSV

**Enunciado:** Exiba todos os sobrenomes de `people.csv`.

**Resposta:**

```bash
cut -d',' -f2 people.csv
```

## 38. Contar os sobrenomes únicos

**Enunciado:** Conte o número de sobrenomes únicos em `people.csv`.

**Resposta:**

```bash
cut -d',' -f2 people.csv | sort -u | wc -l
```

## 39. Excluir o cabeçalho da contagem

**Enunciado:** Verifique se o cabeçalho CSV foi contado por acidente no desafio anterior.

**Resposta:**

```bash
tail -n +2 people.csv | cut -d, -f2 | sort -u | wc -l
```

## 40. Segunda forma de excluir o cabeçalho

**Enunciado:** Encontre uma segunda forma de excluir o cabeçalho CSV da contagem.

**Resposta:**

```bash
sed '1d' people.csv | cut -d, -f2 | sort -u | wc -l
```

## 41. Comparar a eficiência das duas soluções

**Enunciado:** Depois de encontrar duas formas de contar corretamente os sobrenomes únicos de `people.csv`, comprove se uma é mais eficiente, ou mais rápida, do que a outra.

**Resposta:**

```bash
time cut -d',' -f2 people.csv | sort -u | wc -l
```

## 42. Contar pessoas chamadas `Josiah`

**Enunciado:** Conte quantas pessoas têm o primeiro nome `Josiah` em `people.csv`.

**Resposta:**

```bash
grep -c '^Josiah' people.csv
```

## 43. Contar arquivos regulares no diretório

**Enunciado:** Conte a quantidade de arquivos, sem incluir diretórios, no diretório `challenges`.

**Resposta:**

```bash
find challenges -type f | wc -l
```

## 44. Contar subdiretórios no diretório

**Enunciado:** Conte a quantidade de subdiretórios no diretório `challenges`.

**Resposta:**

```bash
find challenges -mindepth 1 -type d | wc -l
```

## 45. Remover todos os arquivos com `deleteme` no nome

**Enunciado:** Remova todos os arquivos cujo nome contém `deleteme`.

**Resposta:**

```bash
find . -type f -name '*deleteme*' -delete
```

## 46. Substituir a frase encontrada no desafio 28

**Enunciado:** No arquivo encontrado no desafio 28, substitua `You found the needle in the haystack!` por `The needle has been removed.`.

**Resposta:** 

```bash
sed -i 's/You found the needle in the haystack!/The needle has been removed./' "$(grep -Rl 'You found the needle in the haystack!' bunch_of_files/ | head -1)"
```

## 47. Converter vírgulas para `|`

**Enunciado:** Converta `people.csv` de delimitado por vírgula para delimitado por `|` e salve o resultado em `people_pipe.csv`.

**Resposta:**

```bash
tr ',' '|' < people.csv > people_pipe.csv
```

## 48. Localizar os duplicados de `file001.rand`

**Enunciado:** Encontre todos os arquivos de `bunch_of_files/` que são duplicados de `file001.rand`.

**Resposta:** O commit final não registrou o comando; ele apenas confirmou a conclusão do desafio.

## 49. Criar e remover o arquivo de nome longo

**Enunciado:** Execute este desafio em exatamente duas etapas: crie um arquivo vazio chamado `supercalifragilisticexpialidocious.txt` e remova-o usando um comando de no máximo cinco caracteres, sem curingas nem globs.

**Resposta:**

```bash
find bunch_of_files/ -type f -exec cmp -s file001.rand {} \; -print
```

## 50. Criar as nove combinações `L-N.txt`

**Enunciado:** Crie arquivos vazios no formato `L-N.txt`, com letras `a`, `b`, `c` e números `1`, `2`, `3`, gerando as nove permutações. Faça o comando o menor possível.

**Resposta:**

```bash
touch {a..c}-{1..3}.txt
```
