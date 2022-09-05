<template>
    <div class="contact-section pb-100">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <div class="contact-text">
                        <h3>¿Tiene alguna pregunta sobre nosotros?</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipiscing elit sed eiusmod tempor incididunt ut labore </p>
                    </div>

                    <div class="contact-form">
                        <form id="contactForm">
                            <div class="form-group">
                                <label>Nombre</label>
                                <input type="text" name="name" id="name" class="form-control" required placeholder="nombre">
                            </div>
                            
                            <div class="form-group">
                                <label>E-mail</label>
                                <input type="email" name="email" id="email" class="form-control" required placeholder="correo">
                            </div>
                            
                            <div class="form-group">
                                <label>Número</label>
                                <input type="text" name="msg_subject" id="msg_subject" class="form-control" required placeholder="número">
                            </div>
                            
                            <div class="form-group">
                                <label>Mensaje</label>
                                <textarea name="message" class="form-control" id="message" cols="30" rows="6" required placeholder="mensaje"></textarea>
                            </div>

                            <div class="send-btn">
                                <button type="submit" class="default-btn">
                                    Enviar mensaje
                                </button>
                            </div>
                        </form>
                    </div>
                </div>

                <div class="col-lg-6">
                    <div class="contact-image">
                        <img src="../../assets/images/contact.png" alt="image">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Contact'
    }
</script>