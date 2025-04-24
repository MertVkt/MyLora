# MyLora
#  ComfyUI Workflow: LoRA Eğitimi & Çoklu Görsel Üretim Rehberi

Bu proje, ComfyUI üzerinde özel LoRA modeli ile çalışacak şekilde tasarlanmış bir görsel üretim workflow'unu ve çoklu prompt sistemiyle birlikte nasıl kullanılacağını gösterir. Kendi veri setimle eğitilmiş bir LoRA modeli örneğiyle birlikte, tüm bileşenlerin nasıl çalıştığını adım adım anlatan rehber bu repoda sunulmuştur.

📺 **Workflow videosunu buradan izleyebilirsiniz (Unlisted):**  
👉 [Workflow Demo ve LoRA Eğitimi Videosu](https://youtu.be/P2NwznjWL-s)

---

##  Gerekli Modeller & Bileşenler

### 🔹 Load Diffusion Model
- **Model Adı:** `flux1-dev.safetensors`

### 🔹 Dual Clip Loader
- **clip_name1:** `t5xxl_fp8_e4m3fn.safetensors`  
- **clip_name2:** `clip_I.safetensors`

### 🔹 Load VAE
- **VAE Adı:** `Flux-dev-ae.safetensors`

### 🔹 Load LoRA
- **LoRA Modeli:** `LORA - mertoqwmxo-julieqwmxo.safetensors`  
- **Trigger Kelimeleri:** <mertoqwmxois>, <julieqwmxo>  
Bu model, kendi veri setimle eğitilmiş olup proje klasöründe yer almaktadır.

---

## 🧾 Çoklu Prompt Kullanımı: `Load prompts from file (inspire)`

Bu node, **çoklu prompt ile çoklu görsel üretimi** için kullanılır. Doğru çalışabilmesi için, promptların bulunduğu bir `.txt` dosyasının aşağıdaki dizinde yer alması gerekir:

```
ComfyUI_windows_portable\ComfyUI\custom_nodes\comfyui-inspire-pack\prompts
```

> ✅ Örnek bir prompt dosyası proje klasörüne dahil edilmiştir.

---

## 🔧 Kurulum ve Kullanım

1. ComfyUI klasörünüzü açın ve gerekli modelleri ilgili klasörlere yerleştirin.
2. `custom_nodes` klasörünüze `comfyui-inspire-pack` node paketi yüklü olmalıdır.
3. `prompts` klasörünüze örnek prompt dosyasını ekleyin ya da kendi prompt listenizi oluşturun.
4. ComfyUI arayüzünden workflow dosyasını yükleyin ve node bağlantılarını kontrol edin.
5. `Trigger Words` kısmına LoRA modeline uygun anahtar kelimeleri kullanarak üretime başlayın.

