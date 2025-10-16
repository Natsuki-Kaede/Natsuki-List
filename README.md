# Intro 

Mixed AD rules for personal use.

# Usage

## AdGuardHome 

### Respond by rcode NOERROR (Recommended)
```
https://testingcf.jsdelivr.net/gh/Natsuki-Kaede/Natsuki-List@main/adguardhome.txt
```

### Legacy
```
https://testingcf.jsdelivr.net/gh/Natsuki-Kaede/Natsuki-List@main/hosts.txt
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
                "url": "https://testingcf.jsdelivr.net/gh/Natsuki-Kaede/Natsuki-List@main/natsuki-list.srs"
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

# License
GPLv3
