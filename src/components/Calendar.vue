<template>
    <div class="calendar">
        <label for="">Date & Time</label>
        <h6 class="month">&lt;<span>July</span>&gt;</h6>
        <div class="wrapper">
            <span>S</span> <span>M</span> <span>T</span> <span>W</span> <span>T</span> <span>F</span> <span>S</span>
            <span class="gray">27</span> <span class="gray">28</span> <span class="gray">29</span> <span
                class="gray">30</span> <span class="gray">31</span> <span>1</span> <span>2</span>
            <span>3</span> <span>4</span> <span>5</span> <span>6</span> <span>7</span> <span>8</span> <span>8</span>
            <span>10</span> <span>11</span> <span>12</span> <span>13</span> <span>14</span> <span>15</span> <span>16</span>
            <span>17</span> <span>18</span> <span>19</span> <span>20</span> <span>21</span> <span>22</span> <span>23</span>
            <span>24</span> <span>25</span> <span>26</span> <span>27</span> <span>28</span> <span>29</span> <span>30</span>
        </div>
    </div>
</template>


<style scoped>
.calendar {
    max-width: max-content;
}


.calendar .wrapper {
    display: grid;
    grid-template-columns: repeat(7, 20px);
    grid-template-rows: repeat(6, 20px);
    grid-column-gap: 30px;
    grid-row-gap: 9px;
    padding: 0;
    margin-top: 6px;
    font-size: .875rem;
    text-align: center;
    padding-bottom: .6em;
    border-bottom: 1px solid #4D4D4D;
}

.calendar .wrapper span:nth-child(-n + 6) {
    font-weight: 600;
}

.calendar .wrapper span:nth-child(n + 8):hover {
    background-color: #FFF;
    color: #000;
    border-radius: 3px;
    cursor: default;
}

.calendar .wrapper span {
    font-weight: 400;
    font-family: 'montserrat', sans-serif;

}

.calendar .month {
    font-size: 1.25rem;
    text-align: center;
    font-family: 'montserrat', sans-serif;
    font-weight: 500;
    border-top: 1px solid #4D4D4D;
    margin-top: 6px;
    padding-top: .6em;
    padding-bottom: .9em;
}

.calendar .month span {
    text-align: center;
    font-family: 'montserrat', sans-serif;
    margin-inline: 2.3em;
}

.calendar .gray {
    color: #4D4D4D;
}

@media (max-width: 400px) {
    .calendar {
        overflow-x: scroll;

    }
}

</style>