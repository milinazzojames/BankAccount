public class BankDriver{
  
  public static void main (String[] args){
      BankAccount nicksAcct = new BankAccount("Nick",450,550);
      BankAccount carolsAcct = new BankAccount("Carol",600,700);
      nicksAcct.printReport();
      carolsAcct.printReport();
      int totalmoney = nicksAcct.getCheckMoney() + nicksAcct.getSaveMoney() + carolsAcct.getCheckMoney() + carolsAcct.getSaveMoney();
      System.out.println("Totally money in all acounts: $" + totalmoney);
      nicksAcct.makeCheckingDeposit(100);
      nicksAcct.printReport();
      carolsAcct.makeCheckingDeposit(nicksAcct.getCheckMoney()); 
      carolsAcct.makeCheckingDeposit(nicksAcct.getSaveMoney());
      nicksAcct.makeCheckingDeposit(-nicksAcct.getCheckMoney());
      nicksAcct.makeSavingsDeposit(-nicksAcct.getSaveMoney());
      nicksAcct.printReport();
      carolsAcct.printReport();
    }
}
