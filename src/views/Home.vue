<template>
<div>
  <div class="home">
    <Sidebar :side="side"/>
  </div>
</div>
</template>

<script>
// @ is an alias to /src
import Sidebar from '@/components/SideBar/NavBar.vue'

export default {
  name: 'Home',
  data () {
    return {
      side: {
        home: {
          show: true,
          route: '/dashboard'
        },
        mensagens: {
          show: false,
          msg: []
        },
        alert: {
          show: true,
          msg: [
            {
              id: 1,
              title: 'Olá sou um alerta',
              route: '',
              body: 'Dia 15 de Abril'
            },
            {
              id: 2,
              title: 'Olá sou um alerta',
              route: '',
              body: 'Dia 19 de Abril'
            }
          ]
        },
        config: {
          show: true,
          route: '/dashboard'
        },
        menu: [
          {
            id: 1,
            nome: 'DashBoard',
            icon: 'far fa-chart-bar',
            route: '/',
            show: false
          },
          {
            id: 4,
            nome: 'Agenda',
            icon: 'far fa-calendar-alt',
            route: '/',
            show: false
          },
          {
            id: 2,
            nome: 'Cadastros',
            icon: 'far fa-address-card',
            route: '',
            show: true,
            sub: [
              {
                nome: 'Pessoas',
                icon: 'far fa-chart-bar',
                route: '',
                show: true,
                sub: [
                  {
                    nome: 'Clientes',
                    icon: 'far fa-chart-bar',
                    route: '/clientes'
                  },
                  {
                    nome: 'Usuários',
                    icon: 'far fa-chart-bar',
                    route: '/usuarios'
                  },
                  {
                    nome: 'Colaboradores',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Fornecedores',
                    icon: 'far fa-chart-bar',
                    route: ''
                  }
                ]
              },
              {
                nome: 'Produtos',
                icon: 'far fa-chart-bar',
                route: '',
                show: true,
                sub: [
                  {
                    nome: 'Produtos',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Grupos',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Armazenamento',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Tipos',
                    icon: 'far fa-chart-bar',
                    route: ''
                  }
                ]
              },
              {
                nome: 'Tabelas',
                icon: 'far fa-chart-bar',
                route: '/',
                show: true,
                sub: [
                  {
                    nome: 'Cidades',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Itens Agenda',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Classes',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    nome: 'Classificação',
                    icon: 'far fa-chart-bar',
                    route: ''
                  }
                ]
              }
            ]
          },
          {
            id: 3,
            nome: 'Financeiro',
            icon: 'far fa-money-bill-alt',
            route: '/',
            show: true,
            sub: [
              {
                id: 3.1,
                nome: 'Caixas',
                icon: 'far fa-chart-bar',
                route: '',
                show: true,
                sub: [
                  {
                    id: '3.1.1',
                    nome: 'Cadastro',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    id: '3.1.2',
                    nome: 'Movimentações',
                    icon: 'far fa-chart-bar',
                    route: ''
                  },
                  {
                    id: '3.1.3',
                    nome: 'Histórico',
                    icon: 'far fa-chart-bar',
                    route: ''
                  }
                ]
              },
              {
                id: 3.2,
                nome: 'Receitas',
                icon: 'far fa-chart-bar',
                route: '/',
                show: false
              },
              {
                id: 3.3,
                nome: 'Despesas',
                icon: 'far fa-chart-bar',
                route: '/',
                show: false
              }
            ]
          },
          {
            id: 6,
            nome: 'PDV',
            icon: 'fa fa-shopping-cart',
            route: '/pdv',
            show: false
          },
          {
            id: 5,
            nome: 'Movimentações',
            icon: 'fas fa-dolly',
            route: '/',
            show: true,
            sub: [
              {
                id: 5.1,
                nome: 'Vendas',
                icon: 'far fa-chart-bar',
                route: '',
                show: false
              },
              {
                id: 5.2,
                nome: 'Compras',
                icon: 'far fa-chart-bar',
                route: '',
                show: false
              }
            ]
          }
        ]
      }
    }
  },
  components: {
    Sidebar
  }
}
</script>
