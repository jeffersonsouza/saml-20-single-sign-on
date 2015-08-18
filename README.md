# SAML 2.0 Single Sign On
Wordpress SAML 2.0 Single Sign on Plugin


Instalação
-----------

Para instalar o Plugin, basta copiar a pasta **saml-20-single-sign-on** para a pasta de plugins do wordpress (geralmente `wp-content/plugins`). Após este passo basta entrar no painel administrativo do wordpress e ativar o plugin.

Configuração
------------
#### General
Na primeira aba é mostrado o status da sua instalaçao e quais parâmetros ainda não estão configurados. Nesta aba você pode habilidar o login sem SAML (passando parâmetros na URL para isso e ativar o funcionamento do SAML em seu site/projeto (após todos os parâmetros obrigatórios serem preenchidos).

#### Identity Provider
Sa segunda aba você precisa configurar os dados de conexão com o seu IdP. Você pode carregar essas informações automáticamente (via XML), usando o campo `Autofill using Metadata` ou informar os campos manualmente.

- IdP name - Nome da sua aplicação no IdP
- Entity ID - entityId cadastrado para a sua aplicação junto ao Service Provider
- URL Identifier - URL do servidor de autenticação
- Single Sign-On URL - URL de autenticação/cadastro
- Single Logout URL - URL de logout
- Certificate Fingerprint - Assinatura do seu arquivo de certificado de conexão com o IdP. VOcê pode usar o comando  `openssl x509 -fingerprint /caminho/do/arquivo.crt` para visualizar a assinatura.

#### Service Provider
##### Authentication
- NameID Policy - Nessa seção você especifica o tipo de autênticação utilizada pelo seu IdP
- Signing Certificate - Seu certificado de autênticação (pode ser gerada no checkbox, caso não tenha)
- Signing Private Key - Sua chave privada para autênticação

##### Attributes
Nesta seção você pode configurar o relacionamento dos campos entro o seu servidor de autênticação e a sua aplicação.

##### Groups
Nesta seção você configura o relacionamento entre os nomes dos grupos de usuário entre o seu servidor de autênticação e a sua aplicação.
