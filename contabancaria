class ContaBancaria:
    def __init__(self, saldo_inicial=0):
        self.saldo = saldo_inicial
        self.transacoes = []

    def depositar(self, valor):
        if valor > 0:
            self.saldo += valor
            self.transacoes.append(f'Depósito: +R${valor:.2f}')
            print(f'Depósito de R${valor:.2f} realizado com sucesso.')
        else:
            print('Valor de depósito deve ser positivo.')

    def sacar(self, valor):
        if valor > 0:
            if self.saldo >= valor:
                self.saldo -= valor
                self.transacoes.append(f'Saque: -R${valor:.2f}')
                print(f'Saque de R${valor:.2f} realizado com sucesso.')
            else:
                print('Saldo insuficiente para saque.')
        else:
            print('Valor de saque deve ser positivo.')

    def extrato(self):
        print('\n--- Extrato ---')
        for transacao in self.transacoes:
            print(transacao)
        print(f'Saldo atual: R${self.saldo:.2f}\n')

# Exemplo de uso
conta = ContaBancaria(100)
conta.depositar(50)
conta.sacar(30)
conta.extrato()
