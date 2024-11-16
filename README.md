class BankAccount {
  String _accountNumber; // Private variable
  double _balance; // Private variable

  BankAccount(this._accountNumber, this._balance);

  String get accountNumber => _accountNumber;

  double get balance => _balance;

  void deposit(double amount) {
    _balance += amount;
  }

  void withdraw(double amount) {
    if (amount <= _balance) {
      _balance -= amount;
    } else {
      print('Insufficient funds!');
    }
  }
}

void main() {
  BankAccount account = BankAccount('123456789', 5000.0);
  account.deposit(1500);
  print('Balance: ${account.balance}');
  account.withdraw(2000);
  print('Balance: ${account.balance}');
}
