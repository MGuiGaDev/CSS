## Modal + Form

![image](https://user-images.githubusercontent.com/82242888/114824544-554a8f80-9dc5-11eb-997e-209661716f42.png)

![image](https://user-images.githubusercontent.com/82242888/114824659-82973d80-9dc5-11eb-8e66-b308ac890f25.png)



```
<div class="container">
  <h2>Fading Modal</h2>
  <p>Add the "fade" class to the modal container if you want the modal to fade in on open and fade out on close.</p>

  <!-- Button to Open the Modal -->
  <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal">
    Open modal
  </button>

  <!-- The Modal -->
  <div class="modal fade" id="myModal">
    <div class="modal-dialog">
        <div class="modal-content">

        <!-- Modal Header -->
        <div class="modal-header">
            <h4 class="modal-title">Iniciar Sesión</h4>
            <button type="button" class="close" data-dismiss="modal">&times;</button>
        </div>

        <!-- Modal body -->
        <div class="modal-body">
            <form action="/action_page.php" class="was-validated">
                <div class="form-group">
                <label for="uname">Nombre de usuario:</label>
                <input type="text" class="form-control" id="uname" placeholder="Enter username" name="uname" required>
                <div class="valid-feedback">Correcto.</div>
                <div class="invalid-feedback">Por favor, rellene este campo.</div>
                </div>
                <div class="form-group">
                    <label for="pwd">Contraseña:</label>
                    <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pswd" required>
                    <div class="valid-feedback">Correcto.</div>
                    <div class="invalid-feedback">Por favor, rellene este campo.</div>
                </div>
                <div class="form-group form-check">
                    <label class="form-check-label">
                    <input class="form-check-input" type="checkbox" name="remember" required> Acepto los términos y condiciones.
                    <div class="valid-feedback">Correcto.</div>
                    <div class="invalid-feedback">Acepte para continuar.</div>
                    </label>
                </div>
                <button type="submit" class="btn btn-primary">Enviar</button>
            </form>
        </div>

        <!-- Modal footer -->
        <div class="modal-footer">
            <button type="button" class="btn btn-danger" data-dismiss="modal">Cerrar</button>
        </div>

        </div>
    </div>
  </div>

</div>
```
