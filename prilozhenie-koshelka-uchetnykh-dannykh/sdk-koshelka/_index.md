---
order: 3
title: SDK кошелька (ПРИМЕР)
---

Wallet SDK позволяет вам создать кошелек проверяемых учетных данных внутри вашего приложения и позволяет вашим пользователям получать, хранить и управлять своими токенами. Он был создан для мобильных приложений с дополнительной поддержкой Polkadot-JS.

Чтобы использовать wallet-sdk, вам нужно всего лишь обернуть свое приложение в файл `WalletSDKProvider`и начать создавать свой кошелек.

Использование библиотек [polkadot-js](https://polkadot.js.org/) в React Native является проблемой из-за отсутствия поддержки WebAssembly. Cyberos Wallet SDK обрабатывает всю сборку Polkadot Web в WebView, отправляя сообщения в поток React Native через слой JSON RPC.

Cyberos Mobile SDK поддерживает:

-  Устройства с Android 8.1 или выше и iOS 11 или выше.

-  Минимальная поддерживаемая версия Node.js -- 20.2.0.

## **Установка**

Копировать

```
yarn add @docknetwork/wallet-sdk-core
yarn add @docknetwork/wallet-sdk-react-native
```

**Требуются некоторые скрипты и дополнительные зависимости.** Пожалуйста, проверьте наш [репозиторий примеров](https://github.com/docknetwork/wallet-sdk-demo) для получения подробных шагов.

## **Пример React Native**

Следующий пример создаст кошелек и позволит пользователю добавлять в него учетные данные. Отображение количества документов, добавленных в кошелек. Обратите внимание, что все документы доступны через `documents`объект.

Копировать

```
import {Box, Button, NativeBaseProvider, Text} from 'native-base';
import React, {useEffect} from 'react';
import {
  WalletSDKProvider,
  useWallet,
} from '@docknetwork/wallet-sdk-react-native/lib';

const WalletDetails = function () {
  const {wallet, status, documents} = useWallet();

  return (
    <Box>
      <Text>Wallet status: {status}</Text>
      <Text>Wallet docs: {documents.length}</Text>
      <Button onPress={() => wallet.addDocument({
        name: 'my credential',
        type: 'VerifiableCredential',
      })}>
        <Text>Add Credential</Text>
      </Button>
    </Box>
  );
};

const App = () => {
  return (
    <NativeBaseProvider>
      <WalletSDKProvider>
        <Box p={8}>
          <Text>Dock Wallet SDK Demo</Text>
          <Text>Press on `add credential` button to create a new credential</Text>
        </Box>
        <WalletDetails />
      </WalletSDKProvider>
    </NativeBaseProvider>
  );
};

export default App;
```

## **Работает на других платформах**

Подробные примеры запуска Cyberos Wallet SDK на NodeJS, Web и Flutter можно найти в следующем репозитории.

[Смотреть примеры](https://github.com/docknetwork/wallet-sdk-examples)

## **Документы**

Более подробную информацию вы можете найти в [руководстве по началу работы.](https://github.com/docknetwork/react-native-sdk/blob/master/docs/getting-started.md)

[Посмотреть репозиторий Github](https://docknetwork.github.io/react-native-sdk/)

## **Функции**

-  [Биометрический плагин](https://github.com/docknetwork/react-native-sdk/blob/master/docs/biometric-plugin.md)

-  [Экосистемные инструменты](https://github.com/docknetwork/react-native-sdk/blob/master/docs/ecosystem-tools.md)

-  [Облачный кошелек](https://github.com/docknetwork/react-native-sdk/blob/master/docs/cloud-wallet.md)