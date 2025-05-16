# Trabalho_Mininet



# Criando topologia linear de 6 Switches com largura de banda de 25Mbps

Execute o seguinte comando no aplicativo PuTTy
```bash
    sudo mn --topo=linear,6 --mac --link tc,bw=25
```


# Informações de interface

Verifique a topologia criada com
```bash
    nodes
```
Verificando os enderecos logicos dos dispositivos da rede.

```bash
    dump
```
 Verificar os enlaces
```bash
    net
```

# Testes de ping


Ping em todos os nós da rede
```bash
    pingall
```
Ping entre h1 e h2
```bash
    h1 ping -c 5 h2
```

Ping entre h3 e h4
```bash
    h3 ping -c 5 h4
```


# Análise de Desempenho

Abrindo os terminais para análise

```bash
    xterm h1 h2
```
Executando os comando em h1

```bash
    iperf -s -p 5555 -i 1    
```

Executando os comando em h2
```bash
    iperf -c 10.0.0.1 -p 5555 -i 1 -t 15   
```
