<template>
    <div class="periodic-table">
        <div class="element" v-for="element in elements" :key="element.symbol || element.spacer">
            <div v-if="element.number">
                <div class="number">{{ element.number }}</div>
                <div class="symbol">{{ element.symbol }}</div>
                <div class="name">{{ element.name }}</div>
                <div class="weight">{{ element.weight }}</div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            elements: [
                { number: 1, symbol: 'H', name: 'Hydrogen', weight: 1.008 },
                { number: 2, symbol: 'He', name: 'Helium', weight: 4.0026 },
                { number: 3, symbol: 'Li', name: 'Lithium', weight: 6.94 },
                { number: 4, symbol: 'Be', name: 'Beryllium', weight: 9.0122 },
                { number: 5, symbol: 'B', name: 'Boron', weight: 10.81 },
                { number: 6, symbol: 'C', name: 'Carbon', weight: 12.011 },
                { number: 7, symbol: 'N', name: 'Nitrogen', weight: 14.007 },
                { number: 8, symbol: 'O', name: 'Oxygen', weight: 15.999 },
                { number: 9, symbol: 'F', name: 'Fluorine', weight: 18.998 },
                { number: 10, symbol: 'Ne', name: 'Neon', weight: 20.180 },
                { number: 11, symbol: 'Na', name: 'Sodium', weight: 22.990 },
                { number: 12, symbol: 'Mg', name: 'Magnesium', weight: 24.305 },
                { number: 13, symbol: 'Al', name: 'Aluminium', weight: 26.982 },
                { number: 14, symbol: 'Si', name: 'Silicon', weight: 28.085 },
                { number: 15, symbol: 'P', name: 'Phosphorus', weight: 30.974 },
                { number: 16, symbol: 'S', name: 'Sulfur', weight: 32.06 },
                { number: 17, symbol: 'Cl', name: 'Chlorine', weight: 35.45 },
                { number: 18, symbol: 'Ar', name: 'Argon', weight: 39.948 },
                { number: 19, symbol: 'K', name: 'Potassium', weight: 39.098 },
                { number: 20, symbol: 'Ca', name: 'Calcium', weight: 40.078 },
                { number: 21, symbol: 'Sc', name: 'Scandium', weight: 44.956 },
                { number: 22, symbol: 'Ti', name: 'Titanium', weight: 47.867 },
                { number: 23, symbol: 'V', name: 'Vanadium', weight: 50.942 },
                { number: 24, symbol: 'Cr', name: 'Chromium', weight: 51.996 },
                { number: 25, symbol: 'Mn', name: 'Manganese', weight: 54.938 },
                { number: 26, symbol: 'Fe', name: 'Iron', weight: 55.845 },
                { number: 27, symbol: 'Co', name: 'Cobalt', weight: 58.933 },
                { number: 28, symbol: 'Ni', name: 'Nickel', weight: 58.693 },
                { number: 29, symbol: 'Cu', name: 'Copper', weight: 63.546 },
                { number: 30, symbol: 'Zn', name: 'Zinc', weight: 65.38 },
                { number: 31, symbol: 'Ga', name: 'Gallium', weight: 69.723 },
                { number: 32, symbol: 'Ge', name: 'Germanium', weight: 72.63 },
                { number: 33, symbol: 'As', name: 'Arsenic', weight: 74.922 },
                { number: 34, symbol: 'Se', name: 'Selenium', weight: 78.971 },
                { number: 35, symbol: 'Br', name: 'Bromine', weight: 79.904 },
                { number: 36, symbol: 'Kr', name: 'Krypton', weight: 83.798 },
                { number: 37, symbol: 'Rb', name: 'Rubidium', weight: 85.468 },
                { number: 38, symbol: 'Sr', name: 'Strontium', weight: 87.62 },
                { number: 39, symbol: 'Y', name: 'Yttrium', weight: 88.906 },
                { number: 40, symbol: 'Zr', name: 'Zirconium', weight: 91.224 },
                { number: 41, symbol: 'Nb', name: 'Niobium', weight: 92.906 },
                { number: 42, symbol: 'Mo', name: 'Molybdenum', weight: 95.95 },
                { number: 43, symbol: 'Tc', name: 'Technetium', weight: 98 },
                { number: 44, symbol: 'Ru', name: 'Ruthenium', weight: 101.07 },
                { number: 45, symbol: 'Rh', name: 'Rhodium', weight: 102.91 },
                { number: 46, symbol: 'Pd', name: 'Palladium', weight: 106.42 },
                { number: 47, symbol: 'Ag', name: 'Silver', weight: 107.87 },
                { number: 48, symbol: 'Cd', name: 'Cadmium', weight: 112.41 },
                { number: 49, symbol: 'In', name: 'Indium', weight: 114.82 },
                { number: 50, symbol: 'Sn', name: 'Tin', weight: 118.71 },
                { number: 51, symbol: 'Sb', name: 'Antimony', weight: 121.76 },
                { number: 52, symbol: 'Te', name: 'Tellurium', weight: 127.6 },
                { number: 53, symbol: 'I', name: 'Iodine', weight: 126.9 },
                { number: 54, symbol: 'Xe', name: 'Xenon', weight: 131.29 },
                { number: 55, symbol: 'Cs', name: 'Caesium', weight: 132.91 },
                { number: 56, symbol: 'Ba', name: 'Barium', weight: 137.33 },
                { number: 57, symbol: 'La', name: 'Lanthanum', weight: 138.91 },
                { number: 58, symbol: 'Ce', name: 'Cerium', weight: 140.12 },
                { number: 59, symbol: 'Pr', name: 'Praseodymium', weight: 140.91 },
                { number: 60, symbol: 'Nd', name: 'Neodymium', weight: 144.24 },
                { number: 61, symbol: 'Pm', name: 'Promethium', weight: 145 },
                { number: 62, symbol: 'Sm', name: 'Samarium', weight: 150.36 },
                { number: 63, symbol: 'Eu', name: 'Europium', weight: 151.96 },
                { number: 64, symbol: 'Gd', name: 'Gadolinium', weight: 157.25 },
                { number: 65, symbol: 'Tb', name: 'Terbium', weight: 158.93 },
                { number: 66, symbol: 'Dy', name: 'Dysprosium', weight: 162.5 },
                { number: 67, symbol: 'Ho', name: 'Holmium', weight: 164.93 },
                { number: 68, symbol: 'Er', name: 'Erbium', weight: 167.26 },
                { number: 69, symbol: 'Tm', name: 'Thulium', weight: 168.93 },
                { number: 70, symbol: 'Yb', name: 'Ytterbium', weight: 173.04 },
                { number: 71, symbol: 'Lu', name: 'Lutetium', weight: 174.97 },
                { number: 72, symbol: 'Hf', name: 'Hafnium', weight: 178.49 },
                { number: 73, symbol: 'Ta', name: 'Tantalum', weight: 180.95 },
                { number: 74, symbol: 'W', name: 'Tungsten', weight: 183.84 },
                { number: 75, symbol: 'Re', name: 'Rhenium', weight: 186.21 },
                { number: 76, symbol: 'Os', name: 'Osmium', weight: 190.23 },
                { number: 77, symbol: 'Ir', name: 'Iridium', weight: 192.22 },
                { number: 78, symbol: 'Pt', name: 'Platinum', weight: 195.08 },
                { number: 79, symbol: 'Au', name: 'Gold', weight: 196.97 },
                { number: 80, symbol: 'Hg', name: 'Mercury', weight: 200.59 },
                { number: 81, symbol: 'Tl', name: 'Thallium', weight: 204.38 },
                { number: 82, symbol: 'Pb', name: 'Lead', weight: 207.2 },
                { number: 83, symbol: 'Bi', name: 'Bismuth', weight: 208.98 },
                { number: 84, symbol: 'Po', name: 'Polonium', weight: 209 },
                { number: 85, symbol: 'At', name: 'Astatine', weight: 210 },
                { number: 86, symbol: 'Rn', name: 'Radon', weight: 222 },
                { number: 87, symbol: 'Fr', name: 'Francium', weight: 223 },
                { number: 88, symbol: 'Ra', name: 'Radium', weight: 226 },
                { number: 89, symbol: 'Ac', name: 'Actinium', weight: 227 },
                { number: 90, symbol: 'Th', name: 'Thorium', weight: 232.04 },
                { number: 91, symbol: 'Pa', name: 'Protactinium', weight: 231.04 },
                { number: 92, symbol: 'U', name: 'Uranium', weight: 238.03 },
                { number: 93, symbol: 'Np', name: 'Neptunium', weight: 237 },
                { number: 94, symbol: 'Pu', name: 'Plutonium', weight: 244 },
                { number: 95, symbol: 'Am', name: 'Americium', weight: 243 },
                { number: 96, symbol: 'Cm', name: 'Curium', weight: 247 },
                { number: 97, symbol: 'Bk', name: 'Berkelium', weight: 247 },
                { number: 98, symbol: 'Cf', name: 'Californium', weight: 251 },
                { number: 99, symbol: 'Es', name: 'Einsteinium', weight: 252 },
                { number: 100, symbol: 'Fm', name: 'Fermium', weight: 257 },
                { number: 101, symbol: 'Md', name: 'Mendelevium', weight: 258 },
                { number: 102, symbol: 'No', name: 'Nobelium', weight: 259 },
                { number: 103, symbol: 'Lr', name: 'Lawrencium', weight: 262 },
                { number: 104, symbol: 'Rf', name: 'Rutherfordium', weight: 267 },
                { number: 105, symbol: 'Db', name: 'Dubnium', weight: 270 },
                { number: 106, symbol: 'Sg', name: 'Seaborgium', weight: 271 },
                { number: 107, symbol: 'Bh', name: 'Bohrium', weight: 270 },
                { number: 108, symbol: 'Hs', name: 'Hassium', weight: 277 },
                { number: 109, symbol: 'Mt', name: 'Meitnerium', weight: 276 },
                { number: 110, symbol: 'Ds', name: 'Darmstadtium', weight: 281 },
                { number: 111, symbol: 'Rg', name: 'Roentgenium', weight: 282 },
                { number: 112, symbol: 'Cn', name: 'Copernicium', weight: 285 },
                { number: 113, symbol: 'Nh', name: 'Nihonium', weight: 286 },
                { number: 114, symbol: 'Fl', name: 'Flerovium', weight: 289 },
                { number: 115, symbol: 'Mc', name: 'Moscovium', weight: 290 },
                { number: 116, symbol: 'Lv', name: 'Livermorium', weight: 293 },
                { number: 117, symbol: 'Ts', name: 'Tennessine', weight: 294 },
                { number: 118, symbol: 'Og', name: 'Oganesson', weight: 294 }
            ]
        };
    }
}
</script>
<style>
.periodic-table {
    display: grid;
    grid-template-columns: repeat(18, 1fr); /* Ensure 18 columns for the periodic table */
    gap: 5px;
    padding: 20px;
    grid-auto-rows: minmax(100px, auto);
    overflow-y: hidden; /* Prevent scrolling overflow below the elements */
}

.element {
    border: 1px solid #ccc;
    padding: 10px;
    text-align: center;
    background-color: #f9f9f9;
    position: relative;
    box-sizing: border-box; /* Ensure padding and border are included in the element's width and height */
}

.number {
    font-size: 0.8em;
    color: #666;
    position: absolute;
    top: 5px;
    left: 5px;
}

.symbol {
    font-size: 1.5em;
    font-weight: bold;
    margin-top: 20px;
}

.name {
    font-size: 0.9em;
    color: #333;
}

.weight {
    font-size: 0.8em;
    color: #999;
    position: absolute;
    bottom: 5px;
    right: 5px;
}

/* Specific positioning for elements to match the typical periodic table layout */
.element:nth-child(1) { grid-column: 1; grid-row: 1; }
.element:nth-child(2) { grid-column: 18; grid-row: 1; }
.element:nth-child(3) { grid-column: 1; grid-row: 2; }
.element:nth-child(4) { grid-column: 2; grid-row: 2; }
.element:nth-child(5) { grid-column: 13; grid-row: 2; }
.element:nth-child(6) { grid-column: 14; grid-row: 2; }
.element:nth-child(7) { grid-column: 15; grid-row: 2; }
.element:nth-child(8) { grid-column: 16; grid-row: 2; }
.element:nth-child(9) { grid-column: 17; grid-row: 2; }
.element:nth-child(10) { grid-column: 18; grid-row: 2; }
.element:nth-child(11) { grid-column: 1; grid-row: 3; }
.element:nth-child(12) { grid-column: 2; grid-row: 3; }
.element:nth-child(13) { grid-column: 13; grid-row: 3; }
.element:nth-child(14) { grid-column: 14; grid-row: 3; }
.element:nth-child(15) { grid-column: 15; grid-row: 3; }
.element:nth-child(16) { grid-column: 16; grid-row: 3; }
.element:nth-child(17) { grid-column: 17; grid-row: 3; }
.element:nth-child(18) { grid-column: 18; grid-row: 3; }
.element:nth-child(19) { grid-column: 1; grid-row: 4; }
.element:nth-child(20) { grid-column: 2; grid-row: 4; }
.element:nth-child(21) { grid-column: 3; grid-row: 4; }
.element:nth-child(22) { grid-column: 4; grid-row: 4; }
.element:nth-child(23) { grid-column: 5; grid-row: 4; }
.element:nth-child(24) { grid-column: 6; grid-row: 4; }
.element:nth-child(25) { grid-column: 7; grid-row: 4; }
.element:nth-child(26) { grid-column: 8; grid-row: 4; }
.element:nth-child(27) { grid-column: 9; grid-row: 4; }
.element:nth-child(28) { grid-column: 10; grid-row: 4; }
.element:nth-child(29) { grid-column: 11; grid-row: 4; }
.element:nth-child(30) { grid-column: 12; grid-row: 4; }
.element:nth-child(31) { grid-column: 13; grid-row: 4; }
.element:nth-child(32) { grid-column: 14; grid-row: 4; }
.element:nth-child(33) { grid-column: 15; grid-row: 4; }
.element:nth-child(34) { grid-column: 16; grid-row: 4; }
.element:nth-child(35) { grid-column: 17; grid-row: 4; }
.element:nth-child(36) { grid-column: 18; grid-row: 4; }
.element:nth-child(37) { grid-column: 1; grid-row: 5; }
.element:nth-child(38) { grid-column: 2; grid-row: 5; }
.element:nth-child(39) { grid-column: 3; grid-row: 5; }
.element:nth-child(40) { grid-column: 4; grid-row: 5; }
.element:nth-child(41) { grid-column: 5; grid-row: 5; }
.element:nth-child(42) { grid-column: 6; grid-row: 5; }
.element:nth-child(43) { grid-column: 7; grid-row: 5; }
.element:nth-child(44) { grid-column: 8; grid-row: 5; }
.element:nth-child(45) { grid-column: 9; grid-row: 5; }
.element:nth-child(46) { grid-column: 10; grid-row: 5; }
.element:nth-child(47) { grid-column: 11; grid-row: 5; }
.element:nth-child(48) { grid-column: 12; grid-row: 5; }
.element:nth-child(49) { grid-column: 13; grid-row: 5; }
.element:nth-child(50) { grid-column: 14; grid-row: 5; }
.element:nth-child(51) { grid-column: 15; grid-row: 5; }
.element:nth-child(52) { grid-column: 16; grid-row: 5; }
.element:nth-child(53) { grid-column: 17; grid-row: 5; }
.element:nth-child(54) { grid-column: 18; grid-row: 5; }
.element:nth-child(55) { grid-column: 1; grid-row: 6; }
.element:nth-child(56) { grid-column: 2; grid-row: 6; }
.element:nth-child(57) { grid-column: 3; grid-row: 9; }
.element:nth-child(58) { grid-column: 4; grid-row: 9; }
.element:nth-child(59) { grid-column: 5; grid-row: 9; }
.element:nth-child(60) { grid-column: 6; grid-row: 9; }
.element:nth-child(61) { grid-column: 7; grid-row: 9; }
.element:nth-child(62) { grid-column: 8; grid-row: 9; }
.element:nth-child(63) { grid-column: 9; grid-row: 9; }
.element:nth-child(64) { grid-column: 10; grid-row: 9; }
.element:nth-child(65) { grid-column: 11; grid-row: 9; }
.element:nth-child(66) { grid-column: 12; grid-row: 9; }
.element:nth-child(67) { grid-column: 13; grid-row: 9; }
.element:nth-child(68) { grid-column: 14; grid-row: 9; }
.element:nth-child(69) { grid-column: 15; grid-row: 9; }
.element:nth-child(70) { grid-column: 16; grid-row: 9; }
.element:nth-child(71) { grid-column: 17; grid-row: 9; }
.element:nth-child(72) { grid-column: 4; grid-row: 6; }
.element:nth-child(73) { grid-column: 5; grid-row: 6; }
.element:nth-child(74) { grid-column: 6; grid-row: 6; }
.element:nth-child(75) { grid-column: 7; grid-row: 6; }
.element:nth-child(76) { grid-column: 8; grid-row: 6; }
.element:nth-child(77) { grid-column: 9; grid-row: 6; }
.element:nth-child(78) { grid-column: 10; grid-row: 6; }
.element:nth-child(79) { grid-column: 11; grid-row: 6; }
.element:nth-child(80) { grid-column: 12; grid-row: 6; }
.element:nth-child(81) { grid-column: 13; grid-row: 6; }
.element:nth-child(82) { grid-column: 14; grid-row: 6; }
.element:nth-child(83) { grid-column: 15; grid-row: 6; }
.element:nth-child(84) { grid-column: 16; grid-row: 6; }
.element:nth-child(85) { grid-column: 17; grid-row: 6; }
.element:nth-child(86) { grid-column: 18; grid-row: 6; }
.element:nth-child(87) { grid-column: 1; grid-row: 7; }
.element:nth-child(88) { grid-column: 2; grid-row: 7; }
.element:nth-child(89) { grid-column: 3; grid-row: 10; }
.element:nth-child(90) { grid-column: 4; grid-row: 10; }
.element:nth-child(91) { grid-column: 5; grid-row: 10; }
.element:nth-child(92) { grid-column: 6; grid-row: 10; }
.element:nth-child(93) { grid-column: 7; grid-row: 10; }
.element:nth-child(94) { grid-column: 8; grid-row: 10; }
.element:nth-child(95) { grid-column: 9; grid-row: 10; }
.element:nth-child(96) { grid-column: 10; grid-row: 10; }
.element:nth-child(97) { grid-column: 11; grid-row: 10; }
.element:nth-child(98) { grid-column: 12; grid-row: 10; }
.element:nth-child(99) { grid-column: 13; grid-row: 10; }
.element:nth-child(100) { grid-column: 14; grid-row: 10; }
.element:nth-child(101) { grid-column: 15; grid-row: 10; }
.element:nth-child(102) { grid-column: 16; grid-row: 10; }
.element:nth-child(103) { grid-column: 17; grid-row: 10; }
.element:nth-child(104) { grid-column: 4; grid-row: 7; }
.element:nth-child(105) { grid-column: 5; grid-row: 7; }
.element:nth-child(106) { grid-column: 6; grid-row: 7; }
.element:nth-child(107) { grid-column: 7; grid-row: 7; }
.element:nth-child(108) { grid-column: 8; grid-row: 7; }
.element:nth-child(109) { grid-column: 9; grid-row: 7; }
.element:nth-child(110) { grid-column: 10; grid-row: 7; }
.element:nth-child(111) { grid-column: 11; grid-row: 7; }
.element:nth-child(112) { grid-column: 12; grid-row: 7; }
.element:nth-child(113) { grid-column: 13; grid-row: 7; }
.element:nth-child(114) { grid-column: 14; grid-row: 7; }
.element:nth-child(115) { grid-column: 15; grid-row: 7; }
.element:nth-child(116) { grid-column: 16; grid-row: 7; }
.element:nth-child(117) { grid-column: 17; grid-row: 7; }
.element:nth-child(118) { grid-column: 18; grid-row: 7; }

/* Responsive design for mobile */
@media (max-width: 768px) {
    .periodic-table {
        grid-template-columns: repeat(4, 1fr); /* Adjust to 4 columns for mobile */
        gap: 2px;
        padding: 10px;
    }

    .element {
        padding: 5px;
        height: auto; /* Allow height to adjust based on content */
    }

    .symbol {
        font-size: 1.2em;
        margin-top: 10px;
    }

    .name, .weight, .number {
        font-size: 0.7em;
    }
}
</style>