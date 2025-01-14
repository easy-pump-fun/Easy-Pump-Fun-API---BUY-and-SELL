Easiest way to buy and sell on pump.fun! Copy, Paste and Run. Focus on your trading algorithm and let Easy Pump Fun handle the rest. Designed with simplicity in mind, it allows you to execute swaps effortlessly just by simply calling the endpoint and providing the necessary parameters. API automatically configures RPC nodes (free for all user), manages all program addresses and token programs, opens and closes token accounts, connects to the bonding curve, handles Compute Units and microLamports, and more.

Check out full docs at [easypumpfun.com](https://www.easypumpfun.com)

ZERO LOG policy ensures that your data stays yours. No tracking. No storage. Ever. To further enhance security, Easy Pump Fun features end-to-end encryption for all requests, IP whitelisting for controlled access (available for subscription plans) and more.

FREE RPC nodes. No setup is required. Free users get access to shared RPC nodes, which means the same nodes are utilized by multiple free-tier users. This makes it possible to offer the service at no cost. These nodes can sometimes experience slower response times, especially during peak usage.

Subscribers get access to dedicated RPC node exclusive to individual account. So there are no bottlenecks caused by other users. Ensuring faster and more reliable performance. Dedicated nodes are automatically assigned to subscribers when they upgrade. No configuration is needed.

PREMIUM API provides advanced features and benefits including dedicated RPC nodes, even faster transaction processing, token sniping functionality, API uptime guarantees, higher rate limits, access to private beta features, priority support and more. To learn more about these features and how to get started, contact support@easypumpfun.com.

For any additional questions feel free to contact support@easypumpfun.com

Check out full docs at [easypumpfun.com](https://www.easypumpfun.com)

Request Example Python - BUY
```

    import requests

    url = "https://www.easypumpfun.com/buy"
    data = {
        "keypair": "2oPQn9z1OaXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXNwt02aoMW7", # [string] Private key for wallet you want to use
        "mint": "9BB6NFEcjBCtnNLFko2FqVQBq8HHM13kCyYcdQbgpump", # [string] Token you want to buy
        "sol_in": 0.5, # [float] Amount of SOL you want to buy with
        "slippage": 2, # [float] Transaction slippage
        "sol_fee": 0.0001 # [float] Fees cost in SOL
        # or you can use compute units and mlamports instead of sol_fee
        # "compute": 100_000,
        # "mlamports": 2_000_000
    }

    response = requests.post(url, json=data)

    print("Status Code:", response.status_code)
    print("Response:", response.json())

```

Request Example Python - SELL
```

    import requests

    url = "https://www.easypumpfun.com/sell"
    data = {
        "keypair": "2oPQn9z1OaXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXNwt02aoMW7", # [string] Private key for wallet you want to use
        "mint": "9BB6NFEcjBCtnNLFko2FqVQBq8HHM13kCyYcdQbgpump", #[string] Token you want to sell
        "percentage": 75, # [float] Amount of SOL you want to buy with
        "slippage": 2, # [float] Transaction slippage
        "sol_fee": 0.0001 # [float] Fees cost in SOL
        # or you can use compute units and mlamports instead of sol_fee
        # "compute": 100_000,
        # "mlamports": 2_000_000
    }

    response = requests.post(url, json=data)

    print("Status Code:", response.status_code)
    print("Response:", response.json())

```

Response 

```
    Status Code: 200 # Successfully connected to endpoint
    "Response:
    { 
        'failed': {
            'message': None, # No fail message
            'status': False # Successfully executed transaction
        },
        'signature': '4ci6dTW6D6ocnKiT8qzD9Bg89wpWx5KeXW2h8JTqeZfk6zKF81AbYUnKuEcTQmdma7Q2mBnutZEW89ZCYpADfzo1'
    }
```

Check out full docs at [easypumpfun.com](https://www.easypumpfun.com)