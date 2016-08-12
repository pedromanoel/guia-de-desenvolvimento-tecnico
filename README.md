# Guia de Desenvolvimento Técnico

[![License](https://img.shields.io/aur/license/yaourt.svg?maxAge=2592000)](https://github.com/ThoughtWorksInc/guia-de-desenvolvimento-tecnico/blob/master/LICENSE)
[![Build Status](https://snap-ci.com/ThoughtWorksInc/guia-de-desenvolvimento-tecnico/branch/master/build_image)](https://snap-ci.com/ThoughtWorksInc/guia-de-desenvolvimento-tecnico/branch/master)

## Visão

* **Para** indivíduos e times
* **Que** buscam desenvolver-se tecnicamente
* **O** Guia de Desenvolvimento Técnico é um guia
* **Que** sugere recursos para crescimento
* **Diferentemente** de outros guias
* **Nosso produto** tem como base as experiências da ThoughtWorks e tem como
  objetivo ensinar não só quem quer entrar na ThoughtWorks mas qualquer
  desenvolvedor.

## Introdução

Esse guia provê dicas e recursos para auxiliar no desenvolvimento de suas
habilidades técnicas através de recursos de aprendizagem já existentes.

Esse guia é para todas as pessoas que desejam aprender como se tornar
melhores desenvolvedoras de software.

## Contribuições

Ficaremos felizes em aceitar contribuições via GitHub pull requests.

## Aviso Legal

Esse não é um guia ou produto oficial da ThoughtWorks Brasil,
mas contém material de propriedade intelectual da mesma.

Esse guia é resultado da compilação de opiniões de funcionários da
ThoughtWorks Brasil e não necessariamente refletem o posicionamento da empresa.

## Segurança

<!--TODO: impartância de pensar em segurança no desenvolvimento de software-->

### Boas práticas de segurança

Check list sobre segurança https://github.com/FallibleInc/security-guide-for-developers

#### Chaves PGP

[PGP](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) :us: (Pretty Good Privacy) é uma implementação que provê criptografica e autenticação de dados.

[GPG](https://pt.wikipedia.org/wiki/GNU_Privacy_Guard) (Gnu Privacy Guard) é a implementação livre do PGP

Tendo um par de chaves GPG é possível encriptar, decriptar e assinar dados, podendo assim manter a segurança e autenticidade dos dados.

#### Chaves SSH

[SSH](https://pt.wikipedia.org/wiki/Secure_Shell) (Secure Shell) é um protocolo para acesso remoto ao shell de forma criptografada.

Recomenda-se utilizar chaves SSH ao invés de senhas para acesso a servidores, repositórios git entre outros.

#### Commit git assinado

Ao fazer commits com a ferramenta git, não há garantias de saber quem é o autor dos commits, sendo que git config não faz nenhum tipo de autenticação durante as configurações.

Um possivel meio para ter garantia na autenticidade dos commits é assinando-os com chave PGP, assim todos e qualquer ferramenta (como o Github por exemplo)
poderá verificar a assinatura do commit.

Efetuar commit assinado [git commit -S](https://git-scm.com/docs/git-commit) :us:
Verificar commits [git verify-commit](https://git-scm.com/docs/git-verify-commit) :us:

#### Gerenciador de senhas

Recomenda-se utilizar gerenciadores de senhas, criar senhas fortes e não utilizar as mesmas senhas para serviços.

Exemplo, ter uma senha com caracteres especiais, letras maiusculas e minusculas e números sendo elas diferentes
para as contas que utilizas (ex. Heroku, Github, SnapCI, etc)

Ferramentas para gerenciador de senhas:

[1Password](https://1password.com/) Ferramenta paga compatível com Mac OS, Windows, Android e IOS
[KeepassX](https://www.keepassx.org/) Ferramenta gratis e open source, com interface gráfica compativel com Linux, Mac OS, Android, IOS
[Pass](https://www.passwordstore.org/) Ferramenta gratis e open source, roda no terminal e utiliza o GPG para criptografar compativel para Linux, Mac OS, Android

#### Gerenciar segredos com o time

Um meio seguro de compartilhar segredos com o time é utilizar gerenciador de senhas compartilhado

Um examplo é usar o [Pass](https://www.passwordstore.org/) que utiliza GPG para encriptar o que permite
que segredos sejam compartilhados para mais de uma pessoa resultando em um único arquivo e o segredos
são sincronizados através do git para ser compartilhado por todos os membros do time

#### Dois fatores de autenticação

Possui dois fatores de autenticação (Two factor authentication) é uma boa pratica para manter maior
segurança no acesso as contas, principalemnte quanto a serviços que podem dar acesso ao codebase ou a
algum ambiente, exemplo: Github, Heroku, SnapCI e etc.

Algumas ferramentas para fazer os dois fatores de autenticação são [Okta](https://www.okta.com/) e [Google Autenticator](https://www.google.com/landing/2step/).

#### OAuth2 para authenticação em APIs

Recomenda-se o uso de OAuth2 para autenticação em APIs, essa mecanismo permite com que apps externos possam se conectar em APIs
sem com que o mesmo saiba a senha do usuário.

Um exemplo para isso é uma app que utiliza a API do Github, essa app basta apenas pedir autorização pelo usuário para acessar
deferminadas informações, no qual o usuário fará utilizando o próprio Github.

Para mais detalhes sobre o OAuth2 no site [http://oauth.net/2/](http://oauth.net/2/) :us:

#### Segurança em aplicações web

Durante o desenvolvimento de aplicações web geralmente são pensandos pontos de usuabilidade e performance,
mas assim como esses itens segurança é algo que deve ser levado em consideração durando o desenvolvimento da
aplicação, um guia para os itens relacionados a segurança é o [OWASP top 10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project) :us:.

Há um PDF em português através do link [OWASP top 10](https://owasptop10.googlecode.com/files/OWASP_Top_10_-_2013_Brazilian_Portuguese.pdf).

#### HTTPS não significa estar seguro

<!--TODO-->

#### Verificação de vulnerabilidades em bibliotecas e pacotes

<!--TODO-->

#### Gerenciando senhas em aplicações

<!--TODO-->
