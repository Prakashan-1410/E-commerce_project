# E-commerce CLI

A Java 17 command-line e-commerce demo with customer, seller, and administrator workflows.

## Features

- Browse products, maintain a cart, and place orders with stock validation.
- Apply percentage coupons; the seeded `WELCOME10` coupon gives 10% off.
- Select card, UPI, net banking, or cash-on-delivery payment strategies. Payments are simulated and no real payment provider is contacted.
- View order history and shipment tracking details.
- Manage seller products, prices, and stock; administrators can update order status and create coupons.
- Keep users, products, coupons, carts, and orders in memory for the lifetime of the process. Restarting clears the data.

## Run

With Maven:

```sh
mvn compile
mvn exec:java -Dexec.mainClass=com.ecommerce.Main
```

Or compile and launch with a JDK 17 installation:

```powershell
javac --release 17 -d target/classes (Get-ChildItem -Recurse src/main/java -Filter *.java | ForEach-Object FullName)
java -cp target/classes com.ecommerce.Main
```

The CLI starts with seeded demo customer, seller, administrator, products, and coupon. Choose a role from the main menu; no login is required in this demo.