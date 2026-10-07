# Documentação do Asset: `audiobtn.png`

Este repositório contém a documentação técnica e as especificações de uso do recurso gráfico `assets/audiobtn.png`, utilizado como elemento de interface do usuário (UI) para botões de controle de áudio e assistente de voz.

## 📋 Visão Geral

O arquivo `audiobtn.png` é um ícone vetorial renderizado, projetado para representar interações de áudio/voz na interface do aplicativo. Ele combina um design visual moderno com metadados de proveniência e autenticidade criptográfica.

## 📐 Especificações Técnicas

| **Propriedade** | **Valor / Descrição** | 
| **Caminho do Arquivo** | `assets/audiobtn.png` | 
| **Resolução / Dimensões** | $716 \times 716$ pixels | 
| **Formato Gráfico** | PNG com vetor SVG preenchido incorporado | 
| **Cor do Vetor** | Monocromático (`fill="black"`) | 
| **Geometria** | Simetria hexagonal com curvas entrelaçadas | 
| **Origem do Asset** | Mídia gerada via algoritmo (IA / OpenAI) | 
| **Padrão de Proveniência** | C2PA (*Coalition for Content Provenance and Authenticity*) v2.2.0 | 

## 🛡️ Autenticidade e Proveniência (Content Credentials)

O arquivo inclui um manifesto criptográfico de proveniência (C2PA) imutável no cabeçalho do arquivo, garantindo a rastreabilidade da sua origem:

* **Agente de Software:** `ChatGPT` / `OpenAI Media Service API`

* **Tipo de Fonte Digital:** `trainedAlgorithmicMedia` (mídia gerada por modelo treinado)

* **Autoridade de Assinatura:** Trufo C2PA Claim Signing CA

## 🚀 Como Utilizar

### 1. Android Native (XML / Jetpack Compose)

Para utilizar o botão em um projeto Android, adicione o arquivo na pasta `res/drawable` ou `assets/`:

**XML Layout:**

```
<ImageButton
    android:id="@+id/btnAudio"
    android:layout_width="48dp"
    android:layout_height="48dp"
    android:background="?attr/selectableItemBackgroundBorderless"
    android:contentDescription="@string/audio_button_desc"
    android:src="@drawable/audiobtn" />

```

### 2. React Native

```
import React from 'react';
import { TouchableOpacity, Image, StyleSheet } from 'react-native';

export const AudioButton = ({ onPress }) => (
  <TouchableOpacity onPress={onPress} style={styles.button}>
    <Image 
      source={require('./assets/audiobtn.png')} 
      style={styles.icon} 
    />
  </TouchableOpacity>
);

const styles = StyleSheet.create({
  button: {
    padding: 10,
  },
  icon: {
    width: 32,
    height: 32,
    resizeMode: 'contain',
  },
});

```

### 3. Web (HTML / CSS)

```
<button class="audio-btn" aria-label="Ativar Áudio">
  <img src="assets/audiobtn.png" alt="Ícone de Áudio" width="32" height="32" />
</button>

```

## 🛠️ Manutenção e Boas Práticas

1. **Acessibilidade:** Lembre-se de sempre definir um texto alternativo (`alt` ou `contentDescription`) adequado para leitores de tela quando utilizar o ícone.

2. **Dimensionamento:** Como o asset possui resolução de $716 \times 716$ px, recomenda-se redimensioná-lo adequadamente de acordo com a densidade de tela do dispositivo alvo para otimizar o uso de memória.