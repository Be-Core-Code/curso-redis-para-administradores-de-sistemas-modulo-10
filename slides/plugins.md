### Plugins

Vamos a instalar el plugin `RedisJSON` para ilustrar cómo podemos ampliar la funcionalidad de Redis
usando plugins

^^^^^^

#### 💻️ Plugins

Clonar el [repositorio que está en Github](https://github.com/RedisJSON/RedisJSON2):

```bash
> git clone https://github.com/RedisJSON/RedisJSON2
```

Instalamos cargo y los paquetes necesarios para compilar el plugin:

```bash
> sudo apk add cargo clang-libs llvm llvm-dev cmake
```

^^^^^^

#### 💻️ Plugins

Construimos el módulo:

```bash
> cd RedisJSON2
> cargo build --release
```
^^^^^^

#### 💻️ Plugins

Cargamos el módulo al iniciar el servidor:

```bash 
> redis-server --loadmodule ./target/release/libredisjson.so 
```

