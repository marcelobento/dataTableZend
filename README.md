# dataTableZend
Customização da DataTable jQuery com Zend 1

# Instalação
Criar um Controller no qual os controlles do zend devem estender. ex
UsuarioController extends MyController

Copiar os métodos 
getRequestDataTable, paginadorDataTable e setJsonDataTable que está no arquivo CustomController.php

Adicionar o Helper GridDataTable para sua pasta de helper

Adicionar a view grid.phtml para dentro da pasta scripts/data-table/grid.phtml

# Como usar
Na view adicionar o trecho de código:
<?php $this->gridDataTable(array(
        'colunas' => $this->colunas, // essa informação vem do controller que está chamando o helper.
        'url' => $this->baseUrl('controller/action')
    ));
?>

# $this->colunas
Mapear o nome do indice que vem do json, e o nome que é adicionado vai ver o nome na grid ex:
<?php array('Nome' => 'nome', 'Idade' => 'idade', 'Cadastro' => 'datacadastro'); ?>

# Action
Verificar a action que está no exemplo.

#OBS
A versão da DataTable é 1.9.4
