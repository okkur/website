+++
fragment = "stripe"
weight = 200
background = "secondary"

post_url = "https://europe-west1-stripe-224618.cloudfunctions.net/stripe/charge"
stripe_token = "pk_live_Pe3txTRxD5WM0Mc79KOxTCM3"

product = "Okkur Research Subscription"

[[prices]]
  text = "$8500/year"
  currency = "usd"

[email]
  label = "Your email address"
+++

*Payment secured and provided by Stripe*