# TonPyLib
# this class use api  https://api.ton.sh/ and  https://toncenter.com/api/test/v1 and will use ton.org api
# use:
``` python
    from Ton import Ton
    import asyncio
    
    async def n():
      async with aiohttp.ClientSession() as session:
        d = Ton(session=session)
        print(await d.getAddressInformation(addres=kQD8uRo6OBbQ97jCx2EIuKm8Wmt6Vb15-KsQHFLbKSMiYHa6) #addres this you wallet )
        #{"ok":true,"result":{"state":"active","balance":19869804595}}
        
        #use proxy
        await d.proxy_session(proxy_url="socks5://3833844140:w61D1u0v@orbtl.s5.opennetwork.cc:999")
        # code
        await d.close()
        
    asyncio.run(n())
```

