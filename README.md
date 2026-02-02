# TOTP

I tried to follow https://datatracker.ietf.org/doc/html/rfc6238 RFC was not very useful. It assumes you know the inner workings of java crypto/mac.
// So it effectively leaves out all the important code if you need to write it in a different language.
// it looks that crypto/mac does all the ipad and opad stuff

crypto="HmacSHA1";
hmac = Mac.getInstance(crypto);
             SecretKeySpec macKey =
                 new SecretKeySpec(keyBytes, "RAW");
             hmac.init(macKey);
             return hmac.doFinal(text);

TOTP: Time-Based One-Time Password Algorithm: https://datatracker.ietf.org/doc/html/rfc6238

HOTP: An HMAC-Based One-Time Password Algorithm: https://datatracker.ietf.org/doc/html/rfc4226

HMAC: Keyed-Hashing for Message Authentication: https://datatracker.ietf.org/doc/html/rfc2104

// https://en.wikipedia.org/wiki/HMAC was much more useful

<a href="https://en.wikipedia.org/wiki/Time-based_one-time_password" target="_blank">https://en.wikipedia.org/wiki/Time-based_one-time_password</a>
<p></p>
<a href="https://datatracker.ietf.org/doc/html/rfc6238" target="_blank">TOTP: Time-Based One-Time Password Algorithm</a>
<p></p>
<a href="https://datatracker.ietf.org/doc/html/rfc2104" target="_blank">HMAC Hashed Message Authentication Code</a>
<p></p>
<a href="https://en.wikipedia.org/wiki/HMAC" target="_blank">HMAC pseudo Code</a>
<p></p>
<a href="https://datatracker.ietf.org/doc/html/rfc4226#section-5.3" target="_blank">Generating an HOTP Value</a>
