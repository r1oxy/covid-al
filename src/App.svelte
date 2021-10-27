<script>

	import { onMount } from "svelte";

	const api = "https://coronavirus-19-api.herokuapp.com/countries/albania";
	let data = {};

	onMount(async () => {
		let rezultati = await fetch(api);
		data = await rezultati.json();
	});


</script>

<main>
	<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
<!-- <span>47:13</span> -->

<div class="container">
    <h2 class="mt-4">Statistika</h2>
    <p>Numrat e përgjithshëm të ndikimit që COVID-19 ka patur në Shqipëri deri tani.
    </p>
    <div class="row">
        <div class="col-6 col-lg-2 mb-2">
            <div class="card shadow-sm">
                <div class="card-body text-center">
					<img src="https://www.publicdomainpictures.net/pictures/320000/velka/coronavirus-infection-clip-art.jpg" alt="" style="max-width: 100%;">
                    <p class="mb-0 lead">ALPETI OSHT GEJ :)))))))))))))))) ALPETI OSHT GEJ :)))) ALPETI OSHT GEJ :))) APLETI OSHT GEJ</p>
                    <h1 class="mb-0">{data.cases}</h1>
                </div>
            </div>
        </div>
        <div class="col-6 col-lg-2 mb-2">
            <div class="card shadow-sm">
                <div class="card-body text-center">
					<img src="https://clipartmag.com/images/white-smiley-face-28.jpg" alt="" style="max-width: 100%; width: 70%; position: relative; top: 20px;">
                    <p class="mb-0 lead" style="position: relative; top: 48px;">Shëruar</p>
                    <h1 class="mb-0 text-success" style="
					display: flex;
					align-content: flex-end;
					height: 60%;
					align-items: center;
					justify-content: center;
				">{data.recovered}</h1>
                </div>
            </div>
        </div>
        <div class="col-6 col-lg-2">
            <div class="card shadow-sm">
                <div class="card-body text-center">
					<img src="https://cdn4.iconfinder.com/data/icons/game-general-icon-set-1/512/skull-512.png" alt="" style="max-width: 100%; width: 100%;">
                    <p class="mb-0 lead" style="position: relative; top: 0px;">Vdekje</p>
                    <h1 class="mb-0 text-danger" 
					style="
					height: 60%;
					align-items: center;
					justify-content: center;
					position: relative:

					"
					
					>{data.deaths}</h1>
                </div>
            </div>
        </div>
		<div class="col-6 col-lg-2 mb-2">
            <div class="card shadow-sm">
                <div class="card-body text-center">
					<img src="https://maxcdn.icons8.com/Share/icon/Dusk_Wired/City/hospital1600.png" alt="" style="max-width: 100%; width: 90%; ">
                    <p class="lead mb-0" style="margin-top: 20px;">Aktive</p>
                    <h1 class="mb-0">{data.active}</h1>
                </div>
            </div>
        </div>
        <div class="col-6 col-lg-2 mb-2">
            <div class="card shadow-sm">
                <div class="card-body text-center">
					<img src="https://clipartart.com/images/at-the-rate-black-clipart-5.jpg" alt="" style="max-width: 100%; width: 90%; position: relative; top: 18px;">
                    <p class="lead mb-0" style="margin-top: 30px;" >Kritike</p>
                    <h1 class="mb-0">{data.critical}</h1>
                </div>
            </div>
        </div>
		<div class="col-6 col-lg-2">
            <div class="card shadow-sm">
                <div class="card-body text-center">
					<img src="https://cdn-icons.flaticon.com/png/512/2841/premium/2841300.png?token=exp=1634745088~hmac=65e5e87092f464b3fa215337497b1759" alt="" style="max-width: 100%; width: 70%; position: relative; top: 18px;">
                    <p class="lead mb-0" style="margin-top: 50px;">Raste në botë/Mln</p>
                    <h1 class="mb-0">{data.casesPerOneMillion}</h1>
                </div>
            </div>
        </div>
    </div>
    <h2 class="mt-4">Sot</h2>
    <p>Shifrat e fundit të ditës së sotme.</p>
    <div class="row">
        <div class="col">
            <div class="card shadow-sm" style="height: 130px;">
                <div class="card-body text-center">
                    <p class="mb-0 lead">Raste</p>
                    <h1 class="mb-0">0</h1>
                </div>
            </div>
        </div>
        <div class="col">
            <div class="card shadow-sm" style="height: 130px;">
                <div class="card-body text-center">
                    <p class="mb-0 lead">Vdekje</p>
                    <h1 class="mb-0">0</h1>
                </div>
            </div>
        </div>
    </div>
</div>


</main>

<style>
	 
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.card {
		height: 280px;
	}
</style>

<!-- C:\Users\Rioni>cd .\Desktop\

C:\Users\Rioni\Desktop>cd .\DS\


C:\Users\Rioni\Desktop\DS>cd .\DigitalSchool\


C:\Users\Rioni\Desktop\DS\DigitalSchool>cd .\Exercises\

C:\Users\Rioni\Desktop\DS\DigitalSchool\Exercises>cd .\my-svelte-project\

C:\Users\Rioni\Desktop\DS\DigitalSchool\Exercises\my-svelte-project>npm install -->
