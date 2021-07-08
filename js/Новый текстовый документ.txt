window.onload = function(){
	const categories = document.querySelectorAll('.navigation__link');
	for(let i = 0; i<=categories.length; i++){
		const card = categories[i];
		card.addEventListener('mouseenter',chooseCategory);
		card.addEventListener('mouseleave',changeCategory)
	}
	

	function chooseCategory(event){
		let id = this.getAttribute('data-id')
		let bg = document.getElementById(id)
		bg.style.opacity = 1;
	}
	function changeCategory(event){
		let id = this.getAttribute('data-id')
		let bg = document.getElementById(id)
		bg.style.opacity = 0;
	}
};