# Waze App

Este repositório contém o MiniWaze, projeto desenvolvidos pelos alunos João Pedro Donasolo, Fernanda e João Lucas Duim como trabalho final para a matéria de Estrutura de Dados e Algorítmos.

As dependências necessárias para a compilação são

* libjsoncpp-dev = 1.7.4-3.1ubuntu2
* libmicrohttpd-dev = 0.9.71-1ubuntu1

Em distribuições linux baseadas em debian:

```
sudo apt-get install libmicrohttpd-dev
sudo apt-get install libjsoncpp-dev
```

Em seguida, para compilar, vá para src/back-end e execute o comando

```
g++ servidor.cpp funcs.cpp structs.cpp -O2 -lmicrohttpd -ljsoncpp -o servidor
```

Se tudo tiver seguido conforme esperado, basta executar o binário *servidor*, abrir uma aba em seu navegador e ir para o endereço [localhost:60000/](calhost:60000/), e o aplicativo deve carregar normalmente.

Também é possível rodar a aplicação pela linha de comando. Para compilar:

```
g++ main.cpp structs.cpp funcs.cpp -o main -O2 -ljsoncpp
```

Quando aberto, o arquivo vai pedir pelo algorítmo a ser usado, assim como por dois pares de latitude e longitude, sendo o primeiro referente ao nó de origem e o segundo ao nó de destino. 