---
layout: post
title: Aula 9 - Redirecionamento de entrada e saida
date:   2022-01-06 14:30:00 +0530
---

Neste capítulo vamos aprender sobre redirecionamento de entrada e saída. Este conteúdo é cobrado no exame de certificação Red Hat RHCSA.

Vamos falar sobre: Redirecionamento de entrada e saída.

Quando você executa este comando:

```
echo hello
```

Tem a saída do comando impressa na tela. Você pode redirecionar a saída para um arquivo usando:

```
echo hello > arquivo.txt
```

Observe:

```
echo hi ! how r u > arquivo.txt
```

Este comando sobrescreveu o arquivo. Para adicionar mais linhas, use:

```
echo hello! I am fine >> arquivo.txt
```

Observe a saída do comando:

```
grep -R juliano /etc
```

Ele teve muita saída de erro, por causa de permissão. 

Agora observe:

```
grep -R juliano /etc 2> /dev/null
```

A saída **2>** é usada para as saídas de erro. E neste caso encaminhamos os erros para um espaço nulo (/dev/null) - *um abismo profundo.* 

```
ls -l /etc/ | grep host
```

Este comando vai listar de forma completa o conteúdo de /etc mas exibir apenas o que inicia com **host**.
