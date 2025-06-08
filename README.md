# Robô Navegador

Este projeto implementa um nó ROS 2 em Python capaz de controlar um robô diferencial no simulador **Stage**, utilizando o sensor **LiDAR** (tópico `/base_scan`) para desviar de obstáculos e alcançar dois pontos-alvo:

- Alvo 1: (x = 7, y = 7)  
- Alvo 2: (x = 7, y = −3)

O controle é feito via envio de comandos de velocidade linear e angular no tópico `/cmd_vel`.

---

## ✅ Requisitos

- ROS 2 Humble
- Python 3.0+
- Dependências:
  - `rclpy`
  - `numpy`
  - `geometry_msgs`

---

## 📦 Instalação e Execução

1. **Baixe o pacote `my_py_pkg`:**  
   [Google Drive - Pacote ROS](https://drive.google.com/drive/folders/1ibeFmYFXh1-7N-63V1m6bfoyLALDRfPm?usp=drive_link)

2. **Substitua os arquivos necessários:**
   - Mundo `.world`: [Google Drive - Arquivo World](https://drive.google.com/drive/folders/1LiETXviGLnBLe0v0EOtiW5HN_tm0Zsbr)
   - Launch corrigido: [GitHub - Launch do Stage](https://github.com/viniciuslg91/stage/tree/main)

3. **Compile o workspace (se necessário):**
   ```bash
   colcon build
   source install/setup.bash
   ```

4. **Execute o ambiente simulado:**
   ```bash
   ros2 launch stage_ros2 stage.launch.py world:=new_cave \
   enforce_prefixes:=false one_tf_tree:=true
   ```

5. **Abra um novo terminal e execute o código do robô:**
   ```bash
   ros2 run my_py_pkg publisher
   ```

---

## 👨‍💻 Autor

- Asaf Ribas  
- Projeto acadêmico - Mestrado em Modelagem Computacional  
- FURG – 2025


---

## 🎥 Demonstração em Vídeo

Confira o funcionamento do robô no vídeo abaixo:  
[https://youtu.be/t_EahCW3DpE](https://youtu.be/t_EahCW3DpE)
