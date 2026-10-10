# Windows Performance Trim & System Recovery

Aplicativo profissional, nativo e portátil para Windows, escrito em C++17, focado em desempenho máximo, redução de overhead do sistema operacional, otimização inteligente de SSDs SATA e NVMe através de 50 blocos avançados, além de ferramentas integradas de recuperação e diagnóstico.

## 🚀 Principais Recursos
- **Interface Gráfica Nativa (Win32 API):** Totalmente responsiva e redimensionável (`WM_SIZE` dinâmico), projetada em arquitetura assíncrona (*multithreaded*) para eliminar qualquer travamento ou *stuttering*.
- **Módulo de 50 Blocos SSD/NVMe Expert:** Seleção individual ou em lote por unidade (`C:`, `D:`, `E:`, etc.) cobrindo TRIM, alinhamento 4K, cache de gravação, filas NVMe e políticas de I/O do Kernel.
- **Elevação UAC Automática:** Verificação e solicitação rigorosa de privilégios administrativos (`runas`) na inicialização.
- **Ferramentas de Diagnóstico e Reparo:** Execução controlada de utilitários nativos de integridade do Windows (`sfc /scannow`).
- **Portabilidade Absoluta:** Sem dependências de runtimes externos (.NET, Python ou bibliotecas pesadas), operando diretamente de pastas locais ou unidades USB.

## 🛠️ Compilação via MinGW-w64 (GCC)
Para compilar o executável de 64 bits (`PerformanceTrim_x64.exe`) diretamente pelo Prompt de Comando ou PowerShell:

```cmd
g++ -std=c++17 -O2 -DNDEBUG -mwindows main.cpp -o PerformanceTrim_x64.exe -lcomctl32 -lshell32 -ladvapi32 -lole32 -lpthread
