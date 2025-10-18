# Intro 

Mixed AD rules for personal use.

# Usage

## AdGuardHome 

### Respond by rcode NOERROR (Recommended)
```
https://github.com/Natsuki-Kaede/Natsuki-List/raw/refs/heads/main/adguardhome.txt
```

### Legacy
```
https://github.com/Natsuki-Kaede/Natsuki-List/raw/refs/heads/main/hosts.txt
```

## Sing-box

``` json
{
    "dns": {
        "rules": [
            {
                "rule_set": [
                    "natsuki-list"
                ],
                "action": "predefined",
                "rcode": "NOERROR"
            }
        ]
    },
    "route": {
        "rules": [
            {
                "rule_set": [
                    "natsuki-list"
                ],
                "action": "reject"
            }
        ],
        "rule_set": [
            {
                "tag": "natsuki-list",
                "type": "remote",
                "format": "binary",
                "url": "https://github.com/Natsuki-Kaede/Natsuki-List/raw/refs/heads/main/natsuki-list.srs"
            }
        ]
    }
}
```

# Upsteam

> [AdguardTeam/AdGuardSDNSFilter](https://github.com/AdguardTeam/AdGuardSDNSFilter)
>
> [Cats-Team/AdRules](https://github.com/Cats-Team/AdRules)
>
> [SukkaW/Surge](https://github.com/SukkaW/Surge)
>
> [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)

# License
GPLv3
