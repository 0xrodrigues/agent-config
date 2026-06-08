## O risco real da fusão

O gate entre Explorer e Refiner não existe por acidente. Ele existe porque **o Explorer pode errar**.

Quando o Explorer erra e você valida, o custo é: você lê o `exploration.md` e corrige.

Quando o Explorer erra dentro de um agente fundido e o Refiner constrói em cima do erro, o custo é: você recebe um `refinement.md` com tarefas baseadas numa leitura incorreta do sistema — e o erro é mais difícil de detectar porque está enterrado numa camada de raciocínio.

**[RISCO]** Em sistemas críticos de core, um `refinement.md` errado que chega ao agente de implementação pode gerar código que parece correto mas está implementando sobre premissas falsas.

Você mesmo disse que o Explorer é confiável quando bem alimentado. Mas "confiável" não é "infalível".
