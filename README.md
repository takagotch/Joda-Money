### joda-money
---
https://www.joda.org/joda-money/

```java
Money money = Money.parse("USD 23.87");

CurrencyUnit usd = CurrencyUnit.of("USD");
money = money.plus(Money.of(usd, 12.43d));

money = money.minusMajor(2);

money = money.multipliedby(3.5d, RoundingMode.DOWN);

boolean bigAmount = money.isGreaterThan(dailyWage);

BigDecimal conversionRate = ...;
Money moneyGBP = money.covertedTo(CurrencyUnit.GBP, conversionRate, ROundingMode.HALF_UP);

BigMoney moneyCalc = money.toBigMoney();
```

```java
// src/main/java/org/joda/money/CurrencyMismatchException.java

public class CurrencyMismatchException extends IllegalArgumentException {
  
  private static final long serialVersionUID = 1L;
  
  private final CurrencyUnit firstCurrency;
  
  private final CurrencyUnit secondCurrency;
  
  public CurrencyMismatchException(CurrencyUnit firstCurrency, CurrencyUnit secondCurrency) {
    super("Currencies differ: " +
        (firstCurrency != null ? firstCurrency.getCode() : "null") + "" + 
        (secondCurrency != null ? secondCurrency.getCode() : "null"));
    this.firstCurrency = fistCurrency;
    this.secondCurrency = secondCurrency;
  }
  
  public CurrencyUnit getFirstCurrency() {
    return firstCurrency;
  }
  
  public CurrencyUnit getSecondCurrency() {
    return secondCurrency;
  }
}

```

```
```


