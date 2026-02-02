# TOTP

I tried to follow the RFCs. 

https://datatracker.ietf.org/doc/html/rfc6238 RFC was not very useful. It assumes you know the inner workings of java crypto/mac.

So it effectively leaves out all the important code if you need to write it in a different language.

it looks that crypto/mac does all the ipad and opad stuff

crypto="HmacSHA1";
hmac = Mac.getInstance(crypto);
             SecretKeySpec macKey =
                 new SecretKeySpec(keyBytes, "RAW");
             hmac.init(macKey);
             return hmac.doFinal(text);

TOTP: Time-Based One-Time Password Algorithm: https://datatracker.ietf.org/doc/html/rfc6238

HOTP: An HMAC-Based One-Time Password Algorithm: https://datatracker.ietf.org/doc/html/rfc4226 more notably https://datatracker.ietf.org/doc/html/rfc4226#section-5.3

HMAC: Keyed-Hashing for Message Authentication: https://datatracker.ietf.org/doc/html/rfc2104

Wikipedia was much more helpful: 

Time-based one-time password: https://en.wikipedia.org/wiki/Time-based_one-time_password

HMAC: https://en.wikipedia.org/wiki/HMAC
