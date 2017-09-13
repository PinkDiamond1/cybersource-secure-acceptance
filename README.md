CyberSource Secure Acceptance
=============================

## Configuration

To run the examples first create a file `config.jsp` under directory `sa-sop` and `sa-wm`

```jsp
-- config.jsp --
<%!

private static final String MERCHANT_ID = "<MERCHANT_ID>";
private static final String PROFILE_ID  = "<PROFILE_ID>";
private static final String ACCESS_KEY  = "<ACCESS_KEY>";
private static final String SECRET_KEY  = "<SECRET_KEY>";

// DF: TEST = 1snn5n9w, LIVE = k8vif92e 
private static final String DF_ORG_ID   = "1snn5n9w";

// PAYMENT URL
private static final String CYBS_BASE_URL = "https://testsecureacceptance.cybersource.com/silent";

private static final String PAYMENT_URL = CYBS_BASE_URL + "/pay";
//private static final String PAYMENT_URL = "debug.jsp";

private static final String TOKEN_CREATE_URL = CYBS_BASE_URL + "/token/create";
private static final String TOKEN_UPDATE_URL = CYBS_BASE_URL + "/token/update";

%>
```

## Run

```term
mvn clean jetty:run
```

## Package

```term
mvn clean package
java -jar target/dependency/jetty-runner.jar target/*.war --path /
```

## Test
 - [http://localhost:8080/sa-sop](http://localhost:8080/sa-sop/)
 - [http://localhost:8080/sa-wm](http://localhost:8080/sa-wm/)

### Test Card
 - http://www.sagepay.co.uk/support/12/36/test-card-details-for-your-test-transactions

## Merchant Login
- URL: https://ebctest.cybersource.com/ebctest/login/Login.do

#### Transaction Search Menu
- Transaction Search > Secure Acceptance Search
- Transaction Search > General Search

